---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: F41E3B17-A33C-4FBF-B532-2E86F1AAE2B8
online version: ''
schema: 2.0.0
ms.openlocfilehash: cf4bc3e4245e3d223d95c3ec5d793a53d5d3bfbe
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046259"
---
# <span data-ttu-id="872a7-101">Import-AzureStorSimpleLegacyApplianceConfig</span><span class="sxs-lookup"><span data-stu-id="872a7-101">Import-AzureStorSimpleLegacyApplianceConfig</span></span>

## <span data-ttu-id="872a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="872a7-102">SYNOPSIS</span></span>
<span data-ttu-id="872a7-103">구성 파일을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="872a7-103">Imports a configuration file.</span></span>

## <span data-ttu-id="872a7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="872a7-104">SYNTAX</span></span>

```
Import-AzureStorSimpleLegacyApplianceConfig -ConfigFilePath <String> -TargetDeviceName <String>
 -ConfigDecryptionKey <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="872a7-105">설명은</span><span class="sxs-lookup"><span data-stu-id="872a7-105">DESCRIPTION</span></span>
<span data-ttu-id="872a7-106">**AzureStorSimpleLegacyApplianceConfig** cmdlet은 레거시 기기에서 구성 파일을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="872a7-106">The **Import-AzureStorSimpleLegacyApplianceConfig** cmdlet imports the configuration file from the legacy appliance.</span></span>
<span data-ttu-id="872a7-107">이 파일에는 Azure StorSimple 서비스에 대 한 볼륨 컨테이너, 백업 정책 및 저장소 계정 자격 증명에 대 한 정보가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="872a7-107">That file contains information about volume containers, backup policies, and storage account credentials for the Azure StorSimple service.</span></span>
<span data-ttu-id="872a7-108">이 cmdlet은 레거시 기기 구성 메타 데이터를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="872a7-108">This cmdlet returns the legacy appliance configuration metadata.</span></span>

## <span data-ttu-id="872a7-109">예제의</span><span class="sxs-lookup"><span data-stu-id="872a7-109">EXAMPLES</span></span>

### <span data-ttu-id="872a7-110">예제 1: 구성 파일 가져오기</span><span class="sxs-lookup"><span data-stu-id="872a7-110">Example 1: Import a configuration file</span></span>
```
PS C:\>Import-AzureStorSimpleLegacyApplianceConfig -ConfigFilePath "C:\MigrationData\LegacyStorSimpleConfig.sse" -TargetDeviceName "8100-123456789" -ConfigDecryptionKey "fWs793hHVhR90NKdDYTeNq"
LegacyConfigId      : e2d5c9b1-b528-4c21-b8ae-533feefc8a41
ImportedOn          : 4/8/2015 7:23:04 PM
ConfigFile          : D:\configs\StorSimpleConfig_27_Mar_15_12_19.xml.sse
TargetApplianceName : Arunkm-N4
Details             : Available Cloud Configuration(s) for migration : 
                          Cloud Configuration(s) 1    : TC8Cloud[Stingray19-FP6] 
                          Cloud Configuration(s) 2    : fulle_cc4
                          Cloud Configuration(s) 3    : fulle_cc2
                          Cloud Configuration(s) 4    : fulle_cc3
                          Cloud Configuration(s) 5    : TC9Cloud[Stingray18-FP3] 
                          Cloud Configuration(s) 6    : fulle_cc1
                          Cloud Configuration(s) 7    : Container-New[Stingray19-FP6] 
                          Cloud Configuration(s) 8    : TC6Cloud[Stingray19-FP6] 
                          Cloud Configuration(s) 9    : TC7Cloud[Stingray18-FP3] 

Result              : Successfully imported config from the legacy appliance! 
Save the legacy config id and cloud configuration(s) for future reference.
```

<span data-ttu-id="872a7-111">이 명령은 지정 된 경로에 있는 구성 파일을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="872a7-111">This command imports the configuration file at the specified path.</span></span>
<span data-ttu-id="872a7-112">명령에는 파일을 해독 하는 키가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="872a7-112">The command includes the key to decrypt the file.</span></span>

## <span data-ttu-id="872a7-113">변수</span><span class="sxs-lookup"><span data-stu-id="872a7-113">PARAMETERS</span></span>

### <span data-ttu-id="872a7-114">-ConfigDecryptionKey</span><span class="sxs-lookup"><span data-stu-id="872a7-114">-ConfigDecryptionKey</span></span>
<span data-ttu-id="872a7-115">레거시 기기의 구성에 대 한 암호 해독 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="872a7-115">Specifies the decryption key for the configuration of the legacy appliance.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="872a7-116">-ConfigFilePath</span><span class="sxs-lookup"><span data-stu-id="872a7-116">-ConfigFilePath</span></span>
<span data-ttu-id="872a7-117">가져올 구성 파일의 절대 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="872a7-117">Specifies the absolute path of the configuration file to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: FilePath

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="872a7-118">-프로필</span><span class="sxs-lookup"><span data-stu-id="872a7-118">-Profile</span></span>
<span data-ttu-id="872a7-119">Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="872a7-119">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="872a7-120">-TargetDeviceName 이름</span><span class="sxs-lookup"><span data-stu-id="872a7-120">-TargetDeviceName</span></span>
<span data-ttu-id="872a7-121">포털에 표시 된 대상 디바이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="872a7-121">Specifies the name of the target device as presented in the portal.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="872a7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="872a7-122">CommonParameters</span></span>
<span data-ttu-id="872a7-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="872a7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="872a7-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="872a7-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="872a7-125">입력</span><span class="sxs-lookup"><span data-stu-id="872a7-125">INPUTS</span></span>

### <span data-ttu-id="872a7-126">않아야</span><span class="sxs-lookup"><span data-stu-id="872a7-126">None</span></span>

## <span data-ttu-id="872a7-127">출력</span><span class="sxs-lookup"><span data-stu-id="872a7-127">OUTPUTS</span></span>

### <span data-ttu-id="872a7-128">LegacyApplianceConfiguration</span><span class="sxs-lookup"><span data-stu-id="872a7-128">LegacyApplianceConfiguration</span></span>
<span data-ttu-id="872a7-129">이 cmdlet은 구성의 세부 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="872a7-129">This cmdlet returns the details of the configuration.</span></span>
<span data-ttu-id="872a7-130">**LegacyApplianceConfiguration** 개체는 구성 ID, 볼륨 컨테이너 이름, 액세스 제어 레코드, 백업 정책, 대역폭 설정, 볼륨 컨테이너, 저장소 계정 자격 증명, 볼륨 등의 정보를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="872a7-130">The **LegacyApplianceConfiguration** object contains the following information: configuration ID, volume container names, access control records, backup policies, bandwidth settings, volume containers, storage account credentials, and volumes.</span></span>

## <span data-ttu-id="872a7-131">상속자</span><span class="sxs-lookup"><span data-stu-id="872a7-131">NOTES</span></span>

## <span data-ttu-id="872a7-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="872a7-132">RELATED LINKS</span></span>

[<span data-ttu-id="872a7-133">가져오기-AzureStorSimpleLegacyVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="872a7-133">Import-AzureStorSimpleLegacyVolumeContainer</span></span>](./Import-AzureStorSimpleLegacyVolumeContainer.md)


