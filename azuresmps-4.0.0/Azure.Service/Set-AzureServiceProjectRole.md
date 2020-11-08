---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 5D093C10-F8B6-4F4A-ABD7-CC4D7AB7AFFA
online version: ''
schema: 2.0.0
ms.openlocfilehash: c78f53b95d18de600535368a1109b318294928c3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045952"
---
# Set-AzureServiceProjectRole

## SYNOPSIS
역할의 인스턴스 수 또는 런타임 버전을 설정 합니다.

## 구문과

### 모두
```
Set-AzureServiceProjectRole [-RoleName <String>] -Instances <Int32> [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### 런타임
```
Set-AzureServiceProjectRole [-RoleName <String>] -Runtime <String> -Version <String> [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### VMSize
```
Set-AzureServiceProjectRole [-RoleName <String>] [-PassThru] -VMSize <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## 설명은
이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.
사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.

**Set-AzureServiceProjectRole** cmdlet은 지정 된 역할에 대 한 역할 인스턴스의 수를 설정 합니다.

## 예제의

### 예제 1: 웹 역할의 인스턴스 설정
```
PS C:\> Set-AzureServiceProjectRole "MyWebRole" 2
```

MyWebRole1 이라는 웹 역할의 인스턴스 수를 2로 설정 합니다.

### 예제 2: 작업자 역할의 인스턴스 설정
```
PS C:\> Set-AzureServiceProjectRole "MyWorkerRole1" 2
```

WorkerRole1 이라는 작업자 역할의 역할 인스턴스 수를 2로 설정 합니다.

### 예제 3: 역할 서비스에 대 한 런타임 버전 설정
```
PS C:\> Set-AzureServiceProjectRole "MyRole1" node 0.6.20
```

역할 MyRole1에 대 한 node.exe 런타임 버전을 0.6.20로 설정 합니다.

## 변수

### -인스턴스
지정 된 웹 또는 작업자 역할에 대 한 역할 인스턴스의 수를 지정 합니다.

```yaml
Type: Int32
Parameter Sets: Instances
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
작업 중인 항목을 나타내는 개체를 반환 합니다.
기본적으로이 cmdlet은 출력을 생성 하지 않습니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -프로필
이 cmdlet이 읽는 Azure 프로필을 지정 합니다.
프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RoleName
변경할 웹 또는 작업자 역할의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### 런타임
지정 된 역할에 추가할 런타임을 지정 합니다.

```yaml
Type: String
Parameter Sets: Runtime
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -버전
역할에 추가할 런타임 버전을 지정 합니다.

```yaml
Type: String
Parameter Sets: Runtime
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMSize
역할의 가상 컴퓨터 크기를 지정 합니다.

```yaml
Type: String
Parameter Sets: VMSize
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

###  
가상 컴퓨터의 크기를 지정 합니다.

## 출력

## 상속자

## 관련 링크

[Set-AzureServiceProject](./Set-AzureServiceProject.md)


