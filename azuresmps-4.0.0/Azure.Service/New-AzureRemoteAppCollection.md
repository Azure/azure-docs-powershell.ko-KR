---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 2021B6BC-7B59-4A88-B1DF-598203F58901
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5e225702238f9a90891db819753a68f728a482f9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045996"
---
# New-AzureRemoteAppCollection

## SYNOPSIS
Azure RemoteApp 컬렉션을 만듭니다.

## 구문과

### AllParameterSets (기본값)
```
New-AzureRemoteAppCollection [-CollectionName] <String> [-ImageName] <String> [-Plan] <String>
 [[-Location] <String>] [-Description <String>] [-CustomRdpProperty <String>] [-ResourceType <CollectionMode>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### AzureVNet
```
New-AzureRemoteAppCollection [-CollectionName] <String> [-ImageName] <String> [-Plan] <String>
 [[-Location] <String>] [-VNetName] <String> [-SubnetName] <String> [-DnsServers <String>] [[-Domain] <String>]
 [[-Credential] <PSCredential>] [-OrganizationalUnit <String>] [-Description <String>]
 [-CustomRdpProperty <String>] [-ResourceType <CollectionMode>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## 설명은
**AzureRemoteAppCollection** Cmdlet은 Azure RemoteApp 컬렉션을 만듭니다.

## 예제의

### 예제 1: 컬렉션 만들기
```
PS C:\> New-AzureRemoteAppCollection -CollectionName "Contoso" -ImageName "Windows Server 2012 R2" -Plan Standard -Location "West US" -Description CloudOnly
```

이 명령은 Azure RemoteApp 컬렉션을 만듭니다.

### 예제 2: 자격 증명을 사용 하 여 컬렉션 만들기
```
PS C:\> $cred = Get-Credential corp.contoso.com\admin
PS C:\> New-AzureRemoteAppCollection -CollectionName "ContosoHybrid" -ImageName "Windows Server 2012 R2" -Plan Standard -VNetName azureVNet -Domain Contoso.com -Credential $cred -Description Hybrid
```

이 명령은 **Get-credential** cmdlet의 자격 증명을 사용 하 여 Azure RemoteApp 컬렉션을 만듭니다.

## 변수

### -CollectionName
Azure RemoteApp 컬렉션의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Credential
사용자의 도메인에 Azure RemoteApp 서버에 가입할 수 있는 권한이 있는 서비스 계정의 자격 증명을 지정 합니다.
**PSCredential** 개체를 가져오려면 **Get-Credential** cmdlet을 사용 합니다.

```yaml
Type: PSCredential
Parameter Sets: AzureVNet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CustomRdpProperty
드라이브 리디렉션 및 기타 설정을 구성 하는 데 사용할 수 있는 사용자 지정 RDP (원격 데스크톱 Protocal) 속성을 지정 합니다.
자세한 내용은 [Windows Server의 원격 데스크톱 서비스에 대 한 RDP 설정을](https://technet.microsoft.com/library/ff393699(v=ws.10).aspx) 참조 `(https://technet.microsoft.com/library/ff393699(v=ws.10).aspx)` 하세요.  

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

### -설명
개체에 대 한 간단한 설명을 지정 합니다.

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

### -DnsServers
DNS 서버의 IPv4 주소 목록 (쉼표로 구분)을 지정 합니다.

```yaml
Type: String
Parameter Sets: AzureVNet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -도메인
RD 세션 호스트 서버에 참가할 Active Directory 도메인 서비스 도메인의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: AzureVNet
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ImageName
Azure RemoteApp 템플릿 이미지의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -위치
컬렉션의 Azure 지역을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OrganizationalUnit
RD 세션 호스트 서버에 가입할 OU (조직 구성 단위)의 이름 (예: OU = MyOu, DC = MyDomain, DC = ParentDomain, DC = com)을 지정 합니다.
OU 및 DC와 같은 특성은 대/소문자를 함께 사용할 수 없습니다.
컬렉션을 만든 후에는 OU를 변경할 수 없습니다.

```yaml
Type: String
Parameter Sets: AzureVNet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -계획
사용 제한을 정의할 수 있는 Azure RemoteApp 컬렉션에 대 한 계획을 지정 합니다.
사용할 수 있는 계획을 보려면 **get-help를 AzureRemoteAppPlan** 를 사용 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
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

### -ResourceType
컬렉션의 리소스 유형을 지정 합니다.
이 매개 변수에 허용 되는 값은 앱 또는 데스크톱입니다.

```yaml
Type: CollectionMode
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SubnetName
Azure RemoteApp 컬렉션을 만드는 데 사용할 가상 네트워크 서브넷의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: AzureVNet
Aliases: 

Required: True
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VNetName
Azure RemoteApp 가상 네트워크의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: AzureVNet
Aliases: 

Required: True
Position: 4
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

[Get-AzureRemoteAppCollection](./Get-AzureRemoteAppCollection.md)

[Get-AzureRemoteAppPlan](./Get-AzureRemoteAppPlan.md)

[제거-AzureRemoteAppCollection](./Remove-AzureRemoteAppCollection.md)

[Set-AzureRemoteAppCollection](./Set-AzureRemoteAppCollection.md)

[업데이트-AzureRemoteAppCollection](./Update-AzureRemoteAppCollection.md)


