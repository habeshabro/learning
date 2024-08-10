```js
import * as THREE from "three";
import {OrbitControls} from "jsm/controls/OrbitControls.js"

//create and insert the renderer
const w  = window.innerWidth;
const h = window.innerHeight;
const renderer = new THREE.WebGLRenderer({antialias: true});
renderer.setSize(w,h);
document.body.appendChild(renderer.domElement);

//create the camera
const fov = 75; // field of view in degree
const aspect = w/h; //aspect ratio
const near = 0.1; //how near for visibility
const far = 10; //how far for visibility
const camera = new THREE.PerspectiveCamera(fov, aspect, near, far);
camera.position.z = 2;

//create the scene
const SomeGroup = new THREE.Group()
const scene = new THREE.Scene();
const controls = new OrbitControls(camera, renderer.domElement);
controls.enableDamping = true;
controls.dampingFactor = 0.03;

const loader = new THREE.TextureLoader();
//create geometry, material and use the two to make an object "mesh"
const geo = new THREE.IcosahedronGeometry(1.0, 2);
const mat = new THREE.MeshStandardMaterial({
    color: 0xffffff,
    flatShading: true,
    map: loader.load("./path/to/jpeg"),
    blending: THREE.AdditiveBlending
})
const mesh = new THREE.Mesh(geo, mat);
scene.add(mesh);

//create and add lighting
const hemiLight = new THREE.HemisphereLight(0x0099ff, 0xaa5500);
scene.add(hemiLight)  

const wireMat = new THREE.MeshBasicMaterial({
    color: 0xffffff,
    wireframe: true
})
const wireMesh = new THREE.Mesh(geo, wireMat);
wireMesh.scale.setScalar(1.001)
mesh.add(wireMesh);


function animate(t=0){
    requestAnimationFrame(animate);
    mesh.rotation.y = t * 0.000;
    mesh.totation.x += 0.002;
    renderer.render(scene, camera);
    controls.update();
}

animate();
```