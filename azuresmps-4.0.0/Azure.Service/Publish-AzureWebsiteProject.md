---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D866554F-78B0-4691-BA06-F625F9B0DFC8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 366941504c020910735015e3d8b282af376d54d9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045877"
---
# Publish-AzureWebsiteProject

## SYNOPSIS
WebDeploy를 사용 하 여 Microsoft Azure 웹 사이트에 Visual Studio 웹 프로젝트를 게시 합니다.

## 구문과

### ProjectFile
```
Publish-AzureWebsiteProject -ProjectFile <String> [-Configuration <String>] [-ConnectionString <Hashtable>]
 [-SkipAppData] [-DoNotDelete] [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### 패키지할
```
Publish-AzureWebsiteProject -Package <String> [-ConnectionString <Hashtable>] [-Tokens <String>]
 [-SetParametersFile <String>] [-SkipAppData] [-DoNotDelete] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
WebDeploy를 사용 하 여 Microsoft Azure 웹 사이트에 Visual Studio 웹 프로젝트를 게시 합니다.
WebDeploy 패키지를 사용 하 고 직접 게시 하거나 Visual Studio 웹 프로젝트를 가져와 프로젝트를 빌드하고 게시할 수 있습니다.
게시 하는 동안 Web.config의 연결 문자열을 바꿀 수도 있습니다.

## 예제의

### 예제 1
```
PS C:\> Publish-AzureWebsiteProject -Name site1 -ProjectFile .\WebApplication1.csproj -Configuration Debug
```

"디버그" 구성을 사용 하 여 Visual Studio 웹 프로젝트 빌드 (Web.Debug.config를 사용 하는 의미) 및 WebDeploy를 사용 하 여 Microsoft Azure 웹 사이트에 게시 합니다.

### 예제 2
```
PS C:\> Publish-AzureWebsiteProject -Name site1 -Package .\WebApplication1.zip
```

Webdeploy를 사용 하 여 WebDeploy 패키지 .zip 파일을 Microsoft Azure 웹 사이트에 게시 합니다.

### 예제 3
```
PS C:\> Publish-AzureWebsiteProject -Name site1 -Package .\WebApplication1
```

Webdeploy를 사용 하 여 Microsoft Azure 웹 사이트에 WebDeploy 패키지 폴더를 게시 합니다.

### 예제 4
```
PS C:\> Publish-AzureWebsiteProject -Name site1 -ProjectFile .\WebApplication1.csproj -ConnectionString @{ DefaultConnection = "my connection string" }
```

Visual Studio 웹 프로젝트를 작성 하 고, Web.config에서 "DefaultConnection" 연결 문자열을 덮어쓰고, WebDeploy를 사용 하 여 Microsoft Azure 웹 사이트에 게시 합니다.

### 예제 5
```
PS C:\> Publish-AzureWebsiteProject -Name site1 -ProjectFile .\WebApplication1.csproj -DefaultConnection "my connection string"
```

Visual Studio 웹 프로젝트를 작성 하 고, Web.config에서 "DefaultConnection" 연결 문자열을 덮어쓰고, WebDeploy를 사용 하 여 Microsoft Azure 웹 사이트에 게시 합니다.
-DefaultConnection은 Web.config 구문 분석을 통해 추가 되는 동적 매개 변수입니다.

## 변수

### -구성
Visual Studio 웹 응용 프로그램 프로젝트를 빌드하는 데 사용 되는 구성입니다.

```yaml
Type: String
Parameter Sets: ProjectFile
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ConnectionString
배포에 사용할 연결 문자열입니다.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DoNotDelete
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

### -이름
웹 사이트 이름입니다.

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

### -패키지
게시할 Visual Studio 웹 응용 프로그램 프로젝트의 zip 파일에 대 한 WebDeploy 패키지 폴더입니다.

```yaml
Type: String
Parameter Sets: Package
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

### -ProjectFile
게시할 Visual Studio 웹 응용 프로그램 프로젝트입니다.

```yaml
Type: String
Parameter Sets: ProjectFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SetParametersFile
```yaml
Type: String
Parameter Sets: Package
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkipAppData
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

### -슬롯
웹 사이트 슬롯 이름입니다.

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

### -토큰
```yaml
Type: String
Parameter Sets: Package
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

[Get-AzureWebsite](./Get-AzureWebsite.md)

[새로운 AzureWebsite](./New-AzureWebsite.md)

[제거-AzureWebsite](./Remove-AzureWebsite.md)

[Set-AzureWebsite](./Set-AzureWebsite.md)


