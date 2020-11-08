---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: CF7E7C62-88FC-48CA-940F-9A6C7442BEF2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8166cd3faa951171dd3ac865b17b8a03bcefdd45
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045883"
---
# Publish-AzureServiceProject

## SYNOPSIS
현재 서비스를 Windows Azure에 게시 합니다.

## 구문과

### # 정의 (기본값)
```
Publish-AzureServiceProject [-ServiceName <String>] [-StorageAccountName <String>] [-Location <String>]
 [-Slot <String>] [-Launch] [-AffinityGroup <String>] [-DeploymentName <String>] [-ForceUpgrade]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### 패키지
```
Publish-AzureServiceProject [-Package <String>] -Configuration <String> [-StorageAccountName <String>]
 [-Location <String>] [-Slot <String>] [-Launch] [-AffinityGroup <String>] [-DeploymentName <String>]
 [-ForceUpgrade] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.
사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.

**게시-AzureServiceProject** cmdlet은 현재 서비스를 클라우드에 게시 합니다.
게시 구성 (예: **구독** , **storageaccountname** , **Location** , **Slot** 등)을 명령줄에 지정 하거나 **Set-azureserviceproject** cmdlet을 통해 로컬 설정에 지정할 수 있습니다.

## 예제의

### 예제 1: 기본 값을 사용 하 여 서비스 프로젝트 게시
```
PS C:\> Publish-AzureServiceProject
```

이 예제에서는 현재 서비스 설정 및 현재 Azure 게시 프로필을 사용 하 여 현재 서비스를 게시 합니다.

### 예제 2: 배포 패키지 만들기
```
PS C:\> Publish-AzureServiceProject -PackageOnly
```

이 예제에서는 서비스 디렉터리에 배포 패키지 (cspkg) 파일을 만들고, Windows Azure에 게시 하지 않습니다.

## 변수

### -AffinityGroup
서비스에 사용 하려는 선호도 그룹을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -구성
서비스 구성 파일을 지정 합니다.
이 매개 변수를 지정 하는 경우 *Package* 매개 변수를 지정 합니다.

```yaml
Type: String
Parameter Sets: PublishFromPackage
Aliases: cc

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DeploymentName
배포 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: dn

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ForceUpgrade
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: f

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -시작
응용 프로그램이 배포 된 후 볼 수 있도록 브라우저 창을 엽니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: ln

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -위치
응용 프로그램이 호스팅되는 영역입니다.
사용할 수 있는 값은 다음과 같습니다. 
  
- 아시아 어디서 나
- 유럽 어디서 나
- 미국 어디서 나
- 동아시아
- 미국 동부
- 대한민국 미국 중부
- 동유럽
- 미국 중부 US
- 동남 아시아
- 유럽 서유럽
- 미국 서 부
 
위치를 지정 하지 않으면 **Set-AzureServiceProject** 에 대 한 마지막 호출에 지정 된 위치가 사용 됩니다. 지정 된 위치가 없으면 위치는 ' 미국 중부 US ' 및 ' 남 중부 US ' 위치에서 임의로 선택 됩니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: l

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -패키지
배포할 패키지 파일을 지정 합니다.
Cspkg 파일 이름 확장명을 가진 로컬 파일 또는 패키지를 포함 하는 blob의 URI를 지정 합니다.
이 매개 변수를 지정 하는 경우 *ServiceName* 매개 변수를 지정 하지 마세요.

```yaml
Type: String
Parameter Sets: PublishFromPackage
Aliases: sp

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

### -ServiceName
Windows Azure에 게시할 때 서비스에 사용할 이름을 지정 합니다.
이름은 cloudapp.net 하위 도메인에서 Windows Azure (cloudapp.net)에 호스트 되는 서비스를 처리 하는 데 사용 되는 레이블의 **일부를 결정** 합니다.
서비스를 게시 하는 동안 지정 된 이름은 서비스를 만들 때 지정 된 이름 보다 우선 합니다.
( **새-AzureServiceProject** cmdlet을 참조 하세요.)

```yaml
Type: String
Parameter Sets: PublishFromServiceDefinition
Aliases: sv

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -슬롯
이 서비스에 사용할 배포 슬롯입니다.
사용할 수 있는 값은 ' 준비 ' 및 ' 생산 '입니다.
슬롯을 지정 하지 않으면 Set-AzureDeploymentSlot에 대 한 마지막 호출에 제공 된 슬롯이 사용 됩니다.
슬롯이 지정 되지 않은 경우 ' 제작 ' 슬롯이 사용 됩니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: sl

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountName
서비스를 게시 하는 동안 사용할 Windows Azure 저장소 계정 이름을 지정 합니다.
이 값은 서비스가 게시 될 때까지 사용 되지 않습니다.
이 매개 변수를 지정 하지 않으면 마지막 **집합-AzureServiceProject** 명령에서 값을 가져옵니다.
저장소 계정이 지정 되지 않은 경우 서비스 이름과 일치 하는 저장소 계정이 사용 됩니다.
이러한 저장소 계정이 없는 경우 cmdlet은 새 계정을 만들려고 시도 합니다.
그러나 서비스 이름과 일치 하는 저장소 계정이 다른 구독에 있으면 시도가 실패할 수 있습니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: st

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

[Enable-AzureServiceProjectRemoteDesktop](./Enable-AzureServiceProjectRemoteDesktop.md)

[Set-AzureServiceProject](./Set-AzureServiceProject.md)


