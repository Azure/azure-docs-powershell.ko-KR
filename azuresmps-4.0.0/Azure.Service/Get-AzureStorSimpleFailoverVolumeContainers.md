---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: BABBA19E-5833-452C-9E36-811EAE7C20F9
online version: ''
schema: 2.0.0
ms.openlocfilehash: cb326281058f0ff9280c4b87c0530241ece801e0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045561"
---
# <span data-ttu-id="36ee1-101">Get-AzureStorSimpleFailoverVolumeContainers</span><span class="sxs-lookup"><span data-stu-id="36ee1-101">Get-AzureStorSimpleFailoverVolumeContainers</span></span>

## <span data-ttu-id="36ee1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36ee1-102">SYNOPSIS</span></span>
<span data-ttu-id="36ee1-103">장치 장애 조치에 대 한 볼륨 컨테이너 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="36ee1-103">Gets the volume container groups for device failover.</span></span>

## <span data-ttu-id="36ee1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="36ee1-104">SYNTAX</span></span>

### <span data-ttu-id="36ee1-105">IdentifyById</span><span class="sxs-lookup"><span data-stu-id="36ee1-105">IdentifyById</span></span>
```
Get-AzureStorSimpleFailoverVolumeContainers -DeviceId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="36ee1-106">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="36ee1-106">IdentifyByName</span></span>
```
Get-AzureStorSimpleFailoverVolumeContainers -DeviceName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="36ee1-107">설명은</span><span class="sxs-lookup"><span data-stu-id="36ee1-107">DESCRIPTION</span></span>
<span data-ttu-id="36ee1-108">**AzureStorSimpleFailoverVolumeContainers** cmdlet은 장치 장애 조치에 대 한 볼륨 컨테이너 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="36ee1-108">The **Get-AzureStorSimpleFailoverVolumeContainers** cmdlet gets the volume container groups for device failover.</span></span>
<span data-ttu-id="36ee1-109">**시작-AzureStorSimpleDeviceFailover** cmdlet에 단일 **VolumeContainer** 그룹 또는 **VolumeContainer** 그룹의 배열을 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="36ee1-109">Pass a single **VolumeContainer** group or an array of **VolumeContainer** groups to the **Start-AzureStorSimpleDeviceFailover** cmdlet.</span></span>
<span data-ttu-id="36ee1-110">**IsDCGroupEligibleForDR** 속성에 대 한 $True 값이 있는 그룹만 장애 조치에 적격 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="36ee1-110">Only groups that have a value of $True for the **IsDCGroupEligibleForDR** property are eligible for failover.</span></span>

## <span data-ttu-id="36ee1-111">예제의</span><span class="sxs-lookup"><span data-stu-id="36ee1-111">EXAMPLES</span></span>

### <span data-ttu-id="36ee1-112">예제 1: 장애 조치 볼륨 컨테이너 가져오기</span><span class="sxs-lookup"><span data-stu-id="36ee1-112">Example 1: Get failover volume containers</span></span>
```
PS C:\>Get-AzureStorSimpleFailoverVolumeContainers -DeviceName "ChewD_App7"

DCGroup                    IneligibilityMessage          IsDCGroupEligibleForDR
-------                    --------------------          ----------------------
{VolumeContainer1889078...                                                 True
{VC_01}                    No cloud snapshot found                        False
{VolumeContainer7306959}   No cloud snapshot found                        False
{VolumeContainer407850151} No cloud snapshot found                        False
```

<span data-ttu-id="36ee1-113">이 명령은 장애 조치 볼륨 컨테이너를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="36ee1-113">This command gets failover volume containers.</span></span>
<span data-ttu-id="36ee1-114">**IsDCGroupEligibleForDR** 속성에 대 한 $True 값이 있는 dcgroups만 장치 장애 조치에 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="36ee1-114">Only the DCGroups that have a value of $True for the **IsDCGroupEligibleForDR** property can be used for device failover.</span></span>

## <span data-ttu-id="36ee1-115">변수</span><span class="sxs-lookup"><span data-stu-id="36ee1-115">PARAMETERS</span></span>

### <span data-ttu-id="36ee1-116">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="36ee1-116">-DeviceId</span></span>
<span data-ttu-id="36ee1-117">Cmdlet을 실행할 StorSimple 장치의 인스턴스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="36ee1-117">Specifies the instance ID of the StorSimple device on which to run the cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36ee1-118">-장치 이름</span><span class="sxs-lookup"><span data-stu-id="36ee1-118">-DeviceName</span></span>
<span data-ttu-id="36ee1-119">Cmdlet을 실행할 StorSimple 장치의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="36ee1-119">Specifies the name of the StorSimple device on which to run the cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36ee1-120">-프로필</span><span class="sxs-lookup"><span data-stu-id="36ee1-120">-Profile</span></span>
<span data-ttu-id="36ee1-121">Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="36ee1-121">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="36ee1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36ee1-122">CommonParameters</span></span>
<span data-ttu-id="36ee1-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="36ee1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36ee1-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36ee1-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36ee1-125">입력</span><span class="sxs-lookup"><span data-stu-id="36ee1-125">INPUTS</span></span>

## <span data-ttu-id="36ee1-126">출력</span><span class="sxs-lookup"><span data-stu-id="36ee1-126">OUTPUTS</span></span>

### <span data-ttu-id="36ee1-127">IList\<DataContainerGroup\></span><span class="sxs-lookup"><span data-stu-id="36ee1-127">IList\<DataContainerGroup\></span></span>
<span data-ttu-id="36ee1-128">이 cmdlet은 **VolumeContainer** 그룹의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="36ee1-128">This cmdlet returns a list of **VolumeContainer** groups.</span></span>

## <span data-ttu-id="36ee1-129">상속자</span><span class="sxs-lookup"><span data-stu-id="36ee1-129">NOTES</span></span>

## <span data-ttu-id="36ee1-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="36ee1-130">RELATED LINKS</span></span>

[<span data-ttu-id="36ee1-131">시작-AzureStorSimpleDeviceFailoverJob</span><span class="sxs-lookup"><span data-stu-id="36ee1-131">Start-AzureStorSimpleDeviceFailoverJob</span></span>](./Start-AzureStorSimpleDeviceFailoverJob.md)

[<span data-ttu-id="36ee1-132">Get-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="36ee1-132">Get-AzureStorSimpleDeviceVolumeContainer</span></span>](./Get-AzureStorSimpleDeviceVolumeContainer.md)


