---
external help file: Azs.AzureBridge.Admin-help.xml
Module Name: Azs.AzureBridge.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c875b28f6518a836296fe1f5f19910d549b880c7
ms.sourcegitcommit: 67e2fac338031c33db27974c89618b614b491b36
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/22/2020
ms.locfileid: "93883301"
---
# Get-AzsAzureBridgeProduct

## SYNOPSIS
Azure Marketplace에서 다운로드할 수 있는 제품 목록을 반환 합니다.

## 구문과

### 목록 (기본값)
```
Get-AzsAzureBridgeProduct -ActivationName <String> -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### 가져오기
```
Get-AzsAzureBridgeProduct -Name <String> -ActivationName <String> -ResourceGroupName <String>
 [<CommonParameters>]
```

### 리소스
```
Get-AzsAzureBridgeProduct -ResourceId <String> [<CommonParameters>]
```

## 설명은
Azure Marketplace에서 다운로드할 수 있는 제품 목록을 반환 합니다.

## 예제의

### 예제 1
```
Get-AzsAzureBridgeProduct -ActivationName 'myActivation' -ResourceGroupName 'activationRG'
```

Azure Marketplace에서 다운로드할 수 있는 제품 목록을 가져옵니다.

### 예제 2
```
Get-AzsAzureBridgeProduct -ActivationName 'myActivation' -ResourceGroupName 'activationRG' -Name 'microsoft.docker-arm.1.1.0'
```

Azure Marketplace에서 이름으로 다운로드 하는 데 사용할 수 있는 제품 정보를 가져옵니다.

## 변수

### -이름
제품의 이름입니다.

```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ActivationName
정품 인증의 이름입니다.

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
리소스가 있는 리소스 그룹입니다.

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
리소스 id입니다.

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -생략
매개 변수 값으로 지정 된 첫 N 개의 항목을 건너뜁니다.

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### -위쪽
매개 변수 값으로 지정 된 대로 상위 N 개 항목을 반환 합니다.
-Skip 매개 변수 뒤에 적용 됩니다.

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

### . Azurestack. 관리자. 제품 리소스

## 상속자

## 관련 링크
