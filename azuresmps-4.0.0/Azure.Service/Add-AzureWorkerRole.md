---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 8632A865-D4CC-4AE5-8307-055CDD776D26
online version: ''
schema: 2.0.0
ms.openlocfilehash: a2b79ee50bb5097896c2a120a9b7316adb2146b5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045710"
---
# Add-AzureWorkerRole

## SYNOPSIS
사용자 지정 작업자 역할에 필요한 파일과 구성을 만듭니다.

## 구문과

```
Add-AzureWorkerRole [-TemplateFolder <String>] [-Name <String>] [-Instances <Int32>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.
사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.

**추가-azure역할** cmdlet은 사용자 지정 작업자 역할에 대해 필요한 파일과 구성을 만듭니다 (스 캐 폴딩이 라고도 함).

## 예제의

### 예제 1: 단일 인스턴스 작업자 역할 만들기
```
PS C:\> Add-AzureWorkerRole -Name MyWorkerRole
```

이 예제에서는 My현 역할 이라는 단일 작업자 역할에 대 한 스 캐 폴딩을 현재 응용 프로그램에 추가 합니다.

### 예제 2: 다중 인스턴스 작업자 역할 만들기
```
PS C:\> Add-AzureWorkerRole MyWorkerRole -I 2
```

이 예제에서는 역할 인스턴스 수가 2 인 Myount 역할 이라는 새 작업자 역할에 대 한 스 캐 폴딩을 현재 응용 프로그램에 추가 합니다.

### 예제 3: 사용자 지정 스 캐 폴딩을 사용 하 여 작업자 역할 만들기
```
PS C:\> Add-AzureWorkerRole MyWorkerRole -TemplateFoldr .\MyWorkerRoleTemplate
```

이 예제에서는 사용자 지정 스 캐 폴딩이 있는 작업자 역할을 만듭니다.

## 변수

### -인스턴스
이 작업자 역할에 대 한 역할 인스턴스의 수를 지정 합니다.
기본값은 1입니다.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: i

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -이름
작업자 역할의 이름을 지정 합니다.
이 값은 작업자 역할에 호스팅되는 사용자 지정 응용 프로그램의 스 캐 폴딩을 포함 하는 폴더 이름을 결정 합니다.
기본값은 WorkerRolenumber 이며, 여기에서 number는 서비스의 작업자 역할 수입니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: n

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

### -서식 폴더
작업자 역할을 만드는 데 사용할 스 캐 폴딩 템플릿 폴더를 지정 합니다.

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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

## 상속자

## 관련 링크

[추가-AzureWebRole](./Add-AzureWebRole.md)

[새로운 AzureRoleTemplate](./New-AzureRoleTemplate.md)


