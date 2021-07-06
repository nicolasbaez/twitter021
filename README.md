## twitter021 | #つぶやきProcessing 
https://twitter.com/nicolasbaez/status/1407163924009689093?s=20

![twitter](https://github.com/nicolasbaez/twitter021/blob/main/twitter021.gif)
```processing
void setup() {
  size(500, 500, P3D);
}
float i, j, k, w=500;
void draw() {
  clear();
  colorMode(RGB, w);
  for (i=50; i<w; i+=50) {
    for (j=50; j<w; j+=50) {
      push();
      translate(i, j);
      rotateX(map(noise(i, j), 0, 1, -k, k));
      sphereDetail(int(noise(i, j)*6));
      fill(i, j, w);
      sphere(20);
      pop();
    }
  }
  k+=0.1;
}
```
