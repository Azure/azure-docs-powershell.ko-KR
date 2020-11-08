---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 79D64D7C-6671-4F03-8776-70A716F36512
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2bc0525ee7238de421842b74f52f7dd4fa59df1a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046261"
---
# Import-AzurePublishSettingsFile

## SYNOPSIS
Windows PowerShell에서 Azure 계정을 관리할 수 있는 게시 설정 파일을 가져옵니다.

## 구문과

```
Import-AzurePublishSettingsFile -PublishSettingsFile <String> [-Environment <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
**가져오기-Azure버전 파일** Cmdlet은 Azure 계정에 대 한 정보가 포함 된 게시 설정 파일 (* publishsettings)을 가져오고 구독 데이터 파일을 컴퓨터에 저장 합니다.
Cmdlet이 완료 되 면 Windows PowerShell에서 Azure 계정을 관리할 수 있습니다.

가져오기 **-Azure# settingsfile** 을 실행 하기 전에 가져올 수 있도록 게시 설정 파일을 다운로드 하 여 저장 하는 **Get-azure# settingsfile** 을 실행 합니다.

Windows PowerShell에서 Azure 계정을 사용할 수 있도록 하려면 게시 설정 파일 또는 **추가-AzureAccount** cmdlet을 사용 하면 됩니다.
게시 설정 파일을 사용 하면 세션을 미리 준비 하 여 스크립트와 백그라운드 작업을 무인 모드로 실행할 수 있습니다.
그러나 모든 서비스에서 설정 파일 게시를 지원 하지는 않습니다.
예를 들어 **AzureResourceManager** 모듈은 게시 설정 파일을 지원 하지 않습니다.

**보안 참고 사항:** 게시 설정 파일에는 인코딩되어 있지만 암호화 되지 않은 관리 인증서가 포함 되어 있습니다.
악의적인 사용자가 게시 설정 파일에 액세스 하는 경우 Azure 서비스를 편집, 만들기, 삭제할 수 있습니다.
최상의 보안을 위해 파일을 다운로드 또는 문서 폴더의 위치에 저장 한 다음 **가져오기-Azure# settingsfile** cmdlet을 사용 하 여 설정을 가져와 삭제 합니다.

## 예제의

### 예제 1: 파일 가져오기
```
PS C:\> Import-AzurePublishSettingsFile -PublishSettingsFile C:\Temp\MyAccount.publishsettings
```

이 명령은 "C:\Temp\MyAccount.publishsettings" 파일을 가져옵니다.

## 변수

### -환경
Azure 환경을 지정 합니다.

Azure 환경에서 글로벌 Azure 용 AzureCloud 및 중국의 21Vianet이 운영 하는 Azure 용 AzureChinaCloud와 같은 Microsoft Azure의 독립 배포입니다.
Azure Pack 및 WAPack cmdlet을 사용 하 여 온-프레미스 Azure 환경을 만들 수도 있습니다.
자세한 내용은 [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  ()을 참조 하세요 https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -프로필
이 cmdlet이 읽는 Azure 프로필을 지정 합니다. 프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.

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

### -# 파일
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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### 않아야
속성 이름으로이 cmdlet에 대 한 입력을 파이프로 지정할 수 있지만 값을 기준으로 하지 않아도 됩니다.

## 출력

### 않아야
이 cmdlet은 출력을 생성 하지 않습니다.

## 상속자
* "게시 설정 파일"은 확장명이 publishsettings 인 XML 파일입니다. 파일에는 Azure 구독에 대 한 관리 자격 증명을 제공 하는 인코딩된 인증서가 포함 되어 있습니다. 이 파일을 가져온 후에는 보안 위험을 방지 하기 위해 삭제 합니다.
* "구독 데이터 파일"은 컴퓨터에 안전 하 게 저장할 수 있는 XML 파일입니다. 기본적으로 사용자 로밍 프로필 ($home/AppData/Roaming)에 저장 됩니다.

## 관련 링크

[Azure PowerShell을 설치 하 고 구성 하는 방법](https://azure.microsoft.com/documentation/articles/install-configure-powershell/)

[추가-AzureAccount](./Add-AzureAccount.md)

[Get-Azure도움말 파일](./Get-AzurePublishSettingsFile.md)


