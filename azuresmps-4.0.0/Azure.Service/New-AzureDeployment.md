---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2BDB255A-EFB3-4580-BE95-187008DB208C
online version: ''
schema: 2.0.0
ms.openlocfilehash: c21195f6d3ed938844717789f8a0df16f49fbd85
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045929"
---
# New-AzureDeployment

## SYNOPSIS
서비스에서 배포를 만듭니다.

## 구문과

```
New-AzureDeployment [-ServiceName] <String> [-Package] <String> [-Configuration] <String> [-Slot] <String>
 [[-Label] <String>] [[-Name] <String>] [-DoNotStart] [-TreatWarningsAsError]
 [-ExtensionConfiguration <ExtensionConfigurationInput[]>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## 설명은
**새-AzureDeployment** cmdlet은 웹 역할 및 작업자 역할로 구성 된 서비스에서 Azure 배포를 만듭니다.
이 cmdlet은 패키지 파일 (cspkg) 및 서비스 구성 파일 (.cscfg)을 기반으로 배포를 만듭니다.
배포 환경 내에서 고유한 이름을 지정 합니다.

**새 add-azurevm** cmdlet을 사용 하 여 Azure 가상 컴퓨터를 기반으로 배포를 만듭니다.

## 예제의

### 예제 1: 배포 만들기
```
PS C:\> New-AzureDeployment -ServiceName "ContosoService" -Slot "Production" -Package "https://contosostorage.blob.core.windows.net/container06/ContosoPackage.cspkg" -Configuration "C:\packages\ContosoConfiguration.cscfg" -Label "ContosoDeployment"
```

이 명령은 ContosoPackage kg 이라는 패키지와 ContosoConfiguration 이라는 구성에 따라 프로덕션 배포를 만듭니다.
명령은 배포에 대 한 레이블을 지정 합니다.
이름은 지정 하지 않습니다.
이 cmdlet은 이름으로 GUID를 만듭니다.

### 예제 2: 확장 구성을 기반으로 배포 만들기
```
PS C:\> New-AzureDeployment -ServiceName "ContosoService" -Slot "Production" -Package "https://contosostorage.blob.core.windows.net/container06/ContosoPackage.cspkg" -Configuration "C:\packages\ContosoConfiguration.cscfg" -ExtensionConfiguration "C:\packages\ContosoExtensionConfig.cscfg"
```

이 명령은 패키지와 구성을 기반으로 프로덕션 배포를 만듭니다.
명령에서 ContosoExtensionConfig 라는 확장 구성을 지정 합니다.
이 cmdlet은 이름 및 레이블로 Guid를 만듭니다.

## 변수

### -구성
서비스 구성 파일의 전체 경로를 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DoNotStart
이 cmdlet이 배포를 시작 하지 않도록 지정 합니다.

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

### -ExtensionConfiguration
확장 구성 개체의 배열을 지정 합니다.

```yaml
Type: ExtensionConfigurationInput[]
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

### -레이블
배포의 레이블 이름을 지정 합니다.
레이블을 지정 하지 않으면이 cmdlet은 GUID를 사용 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -이름
배포 이름을 지정 합니다.
이름을 지정 하지 않으면이 cmdlet은 GUID를 사용 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: DeploymentName

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -패키지
동일한 구독 또는 프로젝트 내의 저장소에서 cspkg 파일의 경로 또는 URI를 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
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

### -ServiceName
배포에 대 한 Azure 서비스의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -슬롯
이 cmdlet이 배포를 만드는 환경을 지정 합니다.
유효한 값은 스테이징 및 프로덕션입니다.
기본값은 실제 값입니다.

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

### -TreatWarningsAsError
경고 메시지가 오류 임을 지정 합니다.
이 매개 변수를 지정 하면 경고 메시지로 인해 배포에 실패 합니다.

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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

## 상속자

## 관련 링크

[다운로드-AzureDeployment](./Get-AzureDeployment.md)

[Get-AzureDeploymentEvent](./Get-AzureDeploymentEvent.md)

[이동-AzureDeployment](./Move-AzureDeployment.md)

[뉴욕](./New-AzureVM.md)

[-AzureDeployment 제거](./Remove-AzureDeployment.md)

[Set AzureDeployment](./Set-AzureDeployment.md)


