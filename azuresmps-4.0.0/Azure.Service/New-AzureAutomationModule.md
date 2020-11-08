---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 1F875179-E3CA-4BBB-822A-600777B2D980
online version: ''
schema: 2.0.0
ms.openlocfilehash: c93a09647e22f9d7f1c69cfd6aafe58799217686
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046223"
---
# New-AzureAutomationModule

## SYNOPSIS

모듈을 자동화로 가져옵니다.

## 구문과

```
New-AzureAutomationModule -Name <String> -ContentLink <Uri> [-Tags <IDictionary>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

**새-AzureAutomationModule** cmdlet은 모듈을 Azure 자동화로 가져옵니다.
모듈은 .zip 확장명을 가진 압축 파일로, 다음 파일 형식 중 하나를 포함 하는 폴더를 포함 합니다.

- Windows PowerShell 모듈 (psm1 파일) 

- Windows PowerShell 모듈 매니페스트 (psd1 파일) 

- 어셈블리 (dll 파일)입니다.

Zip 파일의 이름, zip 파일의 폴더 및 폴더 (psm1, psd. 1 또는 .dll)의 파일이 일치 해야 합니다.

## 예제의

### 예제 1: 모듈 가져오기
```
PS C:\> New-AzureAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLink "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip"
```

이 명령은 ContosoModule 이라는 모듈을 Contoso17 이라는 Automation 계정으로 가져옵니다.
이 모듈은 contosostorage 이라는 저장소 계정의 Azure blob에 저장 되며, 명명 된 컨테이너인 container입니다.

## 변수

### -AutomationAccountName
모듈이 저장 될 자동화 계정의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ContentLink
모듈 파일에 대 한 경로를 지정 하는 웹 사이트 또는 Azure blob 저장소와 같은 공개 URL입니다.
이 위치는 publically 액세스할 수 있어야 합니다.

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -이름
모듈의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### 태그
모듈과 관련 된 하나 이상의 태그를 지정 합니다.

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: Tag

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

### Microsoft Azure. 모듈별. 모듈

## 상속자

## 관련 링크

[Get-AzureAutomationModule](./Get-AzureAutomationModule.md)

[-AzureAutomationModule 제거](./Remove-AzureAutomationModule.md)

[Set AzureAutomationModule](./Set-AzureAutomationModule.md)


