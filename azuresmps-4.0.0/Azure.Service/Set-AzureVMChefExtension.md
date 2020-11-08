---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 021D4624-AE78-4FBE-B1DE-A8A84DF1FC90
online version: ''
schema: 2.0.0
ms.openlocfilehash: 52c3a26887e42884025234ba5f1a7330c258e903
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046045"
---
# Set-AzureVMChefExtension

## SYNOPSIS
가상 컴퓨터에 요리사 확장을 추가 합니다.

## 구문과

### Windows (기본값)
```
Set-AzureVMChefExtension [-Version <String>] -ValidationPem <String> [-ClientRb <String>]
 [-BootstrapOptions <String>] [-RunList <String>] [-JsonAttribute <String>] [-ChefDaemonInterval <String>]
 [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>] [-Windows]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### Linux
```
Set-AzureVMChefExtension [-Version <String>] -ValidationPem <String> [-ClientRb <String>]
 [-BootstrapOptions <String>] [-RunList <String>] [-JsonAttribute <String>] [-ChefDaemonInterval <String>]
 [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>] [-Linux]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## 설명은
**AzureVMChefExtension** cmdlet은 가상 컴퓨터에 요리사 확장을 추가 합니다.

## 예제의

### 예제 1: Windows 가상 컴퓨터에 요리사 확장 추가
```
PS C:\> Set-AzureVMChefExtension -VM $VM -ValidationPem "C:\\myorg-validator.pem" -ClientRb "C:\\client.rb" -RunList "Apache" -Windows;
```

이 명령은 Windows 가상 컴퓨터에 요리사 확장을 추가 합니다.
가상 컴퓨터가 들어오면 요리사를 사용 하 여 부트스트랩 되 고 Apache에서 실행 됩니다.

### 예제 2: 부트스트래핑을 사용 하 여 Windows 가상 컴퓨터에 요리사 확장 추가
```
PS C:\> Set-AzureVMChefExtension -VM $VM -ValidationPem "C:\\myorg-validator.pem" -BootstrapOptions '{"chef_node_name":"your_node_name","chef_server_url":"https://api.opscode.com/organizations/some-org", "validation_client_name":"some-org-validator"}' -RunList "Apache" -Windows;
```

이 명령은 Windows 가상 컴퓨터에 요리사 확장명을 추가 합니다.
가상 컴퓨터가 시작 되 면 요리사를 사용 하 여 부트스트랩 되 고 Apache를 실행 합니다.
부트스트래핑 후 가상 컴퓨터는 JSON 형식으로 지정 된 *BootstrapOptions* 를 참조 합니다.

### 예제 3: Windows 가상 컴퓨터에 요리사 확장 추가 및 Apache 및 GIT 설치
```
PS C:\> Set-AzureVMChefExtension -VM $VM -ValidationPem "C:\\myorg-validator.pem" -ChefServerUrl "http://ipaddress:port" -ValidationClientName "MyOrg-Validator" -RunList "apache, git" -Windows;
```

이 명령은 Windows 가상 컴퓨터에 요리사 확장명을 추가 합니다.
가상 컴퓨터가 시작 되 면 요리사를 사용 하 여 부트스트랩 되며 Apache 및 GIT이 설치 됩니다.
Rb를 제공 하지 않는 경우 요리사 서버 URL 및 유효성 검사 클라이언트 이름을 제공 해야 합니다.

### 예제 4: Linux 가상 컴퓨터에 요리사 확장 추가
```
PS C:\> Set-AzureVMChefExtension -VM $VM -ValidationPem "C:\\myorg-validator.pem" -ChefServerUrl "http://ipaddress:port" -OrganizationName "MyOrg" -Linux;
```

이 명령은 Linux 가상 머신에 요리사 확장명을 추가 합니다.
가상 컴퓨터가 시작 되 면 요리사를 사용 하 여 부트스트랩 됩니다.
Rb를 제공 하지 않는 경우 요리사 서버 URL 및 조직을 제공 해야 합니다.

## 변수

### -BootstrapOptions
JSON (JavaScript Object Notation) 형식의 부트스트랩 옵션을 지정 합니다.

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

### -BootstrapVersion
확장과 함께 설치 된 요리사 클라이언트의 버전을 지정 합니다.

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

### -ChefDaemonInterval
요리사가 실행 되는 빈도 (분 단위)를 지정 합니다. Azure VM에 요리사를 설치 하지 않으려는 경우에는이 필드에서 값을 0으로 설정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ChefServiceInterval

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ChefServerUrl
요리사 서버의 URL을 지정 합니다.

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

### -ClientRb
요리사 클라이언트. rb의 전체 경로를 지정 합니다.

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

### -데몬
무인 실행을 요리사 클라이언트 서비스를 구성 합니다. 노드 플랫폼은 Windows 여야 합니다.
허용 되는 옵션: ' 없음 ', ' 서비스 ' 및 ' 작업 '.
없음-현재 요리사-클라이언트 서비스가 서비스로 구성 되는 것을 방지 합니다.
서비스-백그라운드에서 서비스로 자동 실행 되도록 요리사 클라이언트를 구성 합니다.
작업-secheduled 작업으로 백그라운드에서 자동으로 실행 되도록 요리사 클라이언트를 구성 합니다.

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

### -InformationAction
이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.

이 매개 변수에 허용 되는 값은 다음과 같습니다.

- 하기로
- 숨기기
- Inquire
- SilentlyContinue
- 중지가
- 대기

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
정보 변수를 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JsonAttribute
요리사의 첫 번째 실행에 추가할 JSON 문자열입니다. 예:-JsonAttribute ' {"foo": "bar"} '

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

### -Linux
이 cmdlet이 Linux 기반 가상 컴퓨터를 생성 함을 나타냅니다.

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OrganizationName
요리사 확장의 조직 이름을 지정 합니다.

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

### -RunList
요리사 노드 실행 목록을 지정 합니다.

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

### -비밀
데이터 모음 항목 값을 암호화 하 고 암호를 해독 하는 데 사용 되는 암호화 키입니다.

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

### -SecretFile
데이터 모음 항목 값을 암호화 하 고 해독 하는 데 사용 되는 암호화 키가 포함 된 파일의 경로입니다.

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

### -ValidationClientName
유효성 검사 클라이언트의 이름을 지정 합니다.

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

### -ValidationPem
요리사 유효성 검사기. pem 파일 경로를 지정 합니다.

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

### -버전
요리사 확장명의 버전 번호를 지정 합니다.

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

### -VM
영구 가상 머신 개체를 지정 합니다.

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Windows
이 cmdlet이 Windows 가상 컴퓨터를 생성 함을 나타냅니다.

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

## 상속자

## 관련 링크

[Get-AzureVMChefExtension](./Get-AzureVMChefExtension.md)

[제거-AzureVMChefExtension](./Remove-AzureVMChefExtension.md)


