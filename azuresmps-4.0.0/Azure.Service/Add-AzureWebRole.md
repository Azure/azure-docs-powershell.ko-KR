---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: FB5CD696-108D-4A3E-8983-1C6562E8795A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 25ade8ccf395d37ab0856742fe473a6508c9d63b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045711"
---
# Add-AzureWebRole

## SYNOPSIS
웹 작업자 역할을 추가 합니다.

## 구문과

```
Add-AzureWebRole [-TemplateFolder <String>] [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## 설명은
이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.
사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.

**추가-AzureWebRole** cmdlet은 웹 작업자 역할을 추가 합니다.

## 예제의

### 예제 1: 기본 역할 추가
```
PS C:\> Add-AzureWebRole
```

이 명령은 Webrole1의 기본 구성이 있는 웹 역할을 이름 및 단일 인스턴스로 추가 합니다.

### 예제 2: 이름을 사용 하 여 역할 추가
```
PS C:\> Add-AzureWebRole -Name "MyWebRole"
```

이 명령은 MyWebRole 이라는 단일 웹 역할을 현재 응용 프로그램에 추가 합니다.

### 예제 3: 이름 및 인스턴스 수를 사용 하 여 역할 추가
```
PS C:\> Add-AzureWebRole -Name "MyWebRole" -Instance 2
```

이 명령은 MyWebRole 이라는 웹 역할을 현재 응용 프로그램에 추가 합니다.
Cmdlet의 역할 인스턴스 수는 2입니다.

### 예제 4: 이름 및 서식 파일을 사용 하 여 역할 추가
```
PS C:\> Add-AzureWebRole -Name "MyWebRole" -TemplateFolder ".\MyWebTemplateFolder"
```

이 명령은 MyWebRole 이라는 단일 웹 역할을 현재 응용 프로그램에 추가 합니다.
명령에서 Myweb서식 파일 폴더를 스 캐 폴딩 템플릿으로 지정 합니다.

## 변수

### -인스턴스
인스턴스 수를 지정 합니다.

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
웹 역할의 이름을 지정 합니다.

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
서식 파일 폴더를 지정 합니다.

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

[추가-Azure역할](./Add-AzureWorkerRole.md)

[새로운 AzureRoleTemplate](./New-AzureRoleTemplate.md)


