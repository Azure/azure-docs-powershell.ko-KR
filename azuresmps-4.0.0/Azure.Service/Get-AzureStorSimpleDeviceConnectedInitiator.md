---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 9436E1AB-870F-4717-ABE0-55A90C07F7E4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 555ce014bbbf7174b3f7142cf7e2f217317eadc6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046291"
---
# <span data-ttu-id="4053b-101">Get-AzureStorSimpleDeviceConnectedInitiator</span><span class="sxs-lookup"><span data-stu-id="4053b-101">Get-AzureStorSimpleDeviceConnectedInitiator</span></span>

## <span data-ttu-id="4053b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4053b-102">SYNOPSIS</span></span>
<span data-ttu-id="4053b-103">StorSimple 장치에 사용할 수 있는 iSCSI 연결을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4053b-103">Gets the iSCSI connections available for a StorSimple device.</span></span>

## <span data-ttu-id="4053b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4053b-104">SYNTAX</span></span>

### <span data-ttu-id="4053b-105">IdentifyById</span><span class="sxs-lookup"><span data-stu-id="4053b-105">IdentifyById</span></span>
```
Get-AzureStorSimpleDeviceConnectedInitiator -DeviceId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="4053b-106">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="4053b-106">IdentifyByName</span></span>
```
Get-AzureStorSimpleDeviceConnectedInitiator -DeviceName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="4053b-107">설명은</span><span class="sxs-lookup"><span data-stu-id="4053b-107">DESCRIPTION</span></span>
<span data-ttu-id="4053b-108">**AzureStorSimpleDeviceConnectedInitiator** Cmdlet은 StorSimple 장치에 사용할 수 있는 iSCSI 연결 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4053b-108">The **Get-AzureStorSimpleDeviceConnectedInitiator** cmdlet gets a list of the iSCSI connections available for a StorSimple device.</span></span>
<span data-ttu-id="4053b-109">이 cmdlet이 반환 하는 iSCSI 연결 개체에는 다음 속성이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4053b-109">The iSCSI connection objects that this cmdlet returns contain the following properties:</span></span>

- <span data-ttu-id="4053b-110">**AcrInstanceId**</span><span class="sxs-lookup"><span data-stu-id="4053b-110">**AcrInstanceId**</span></span>
- <span data-ttu-id="4053b-111">**AcrName**</span><span class="sxs-lookup"><span data-stu-id="4053b-111">**AcrName**</span></span>
- <span data-ttu-id="4053b-112">**AllowedVolumeNames**</span><span class="sxs-lookup"><span data-stu-id="4053b-112">**AllowedVolumeNames**</span></span>
- <span data-ttu-id="4053b-113">**InitiatorAddress**</span><span class="sxs-lookup"><span data-stu-id="4053b-113">**InitiatorAddress**</span></span>
- <span data-ttu-id="4053b-114">**인터페이스**</span><span class="sxs-lookup"><span data-stu-id="4053b-114">**Interfaces**</span></span>
- <span data-ttu-id="4053b-115">**Iqn**</span><span class="sxs-lookup"><span data-stu-id="4053b-115">**Iqn**</span></span>
- <span data-ttu-id="4053b-116">**IscsiConnectionId**</span><span class="sxs-lookup"><span data-stu-id="4053b-116">**IscsiConnectionId**</span></span>

<span data-ttu-id="4053b-117">이 cmdlet은 디바이스에 대해 iSCSI 연결이 설정 된 경우에만 연결 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4053b-117">This cmdlet gets connection object only if iSCSI connections are turned on for the device.</span></span>
<span data-ttu-id="4053b-118">기본적으로 연결은 꺼집니다.</span><span class="sxs-lookup"><span data-stu-id="4053b-118">By default, connections are turned off.</span></span>

## <span data-ttu-id="4053b-119">예제의</span><span class="sxs-lookup"><span data-stu-id="4053b-119">EXAMPLES</span></span>

### <span data-ttu-id="4053b-120">예제 1: 장치에 대 한 모든 연결 가져오기</span><span class="sxs-lookup"><span data-stu-id="4053b-120">Example 1: Get all connections for a device</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceConnectedInitiator -DeviceName "Contoso63-AppVm"
VERBOSE: ClientRequestId: bec615b9-79ab-4671-88b0-287adeb6bf68_PS
VERBOSE: ClientRequestId: ef976c58-2660-41c8-aa15-c84e70c9d01c_PS
VERBOSE: ClientRequestId: 9b306b96-8e76-47ed-beda-d3bd2fb2bb82_PS
VERBOSE: ClientRequestId: 0f4fc743-0b60-45da-a45a-27f4b0f32bd2_PS

AcrInstanceId      : 55f24643-ab3a-4098-ade2-aa2b1a3ab18c
AcrName            : Contoso63-AppVm
AllowedVolumeNames : {Policyvolume1_Default}
InitiatorAddress   : 
Interfaces         : {Data0}
Iqn                : iqn10
IscsiConnectionId  : cfc144cb-00f1-44b1-9655-80b431f2161b

VERBOSE: 1 Iscsi Connection found!
```

<span data-ttu-id="4053b-121">이 명령은 Contoso63 라는 장치에 대 한 모든 iSCSI 연결을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4053b-121">This command gets all iSCSI connections for the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="4053b-122">이 명령은 장치에 대 한 연결이 설정 된 경우에만 연결을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="4053b-122">This command returns connections only if connections are turned on for the device.</span></span>

## <span data-ttu-id="4053b-123">변수</span><span class="sxs-lookup"><span data-stu-id="4053b-123">PARAMETERS</span></span>

### <span data-ttu-id="4053b-124">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="4053b-124">-DeviceId</span></span>
<span data-ttu-id="4053b-125">ISCSI 초기자를 가져올 StorSimple 장치의 인스턴스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4053b-125">Specifies the instance ID of the StorSimple device from which to get iSCSI initiators.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: ID

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4053b-126">-장치 이름</span><span class="sxs-lookup"><span data-stu-id="4053b-126">-DeviceName</span></span>
<span data-ttu-id="4053b-127">ISCSI 초기자를 가져올 StorSimple 장치의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4053b-127">Specifies the name of the StorSimple device from which to get iSCSI initiators.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4053b-128">-프로필</span><span class="sxs-lookup"><span data-stu-id="4053b-128">-Profile</span></span>
<span data-ttu-id="4053b-129">Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4053b-129">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="4053b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4053b-130">CommonParameters</span></span>
<span data-ttu-id="4053b-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4053b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4053b-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4053b-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4053b-133">입력</span><span class="sxs-lookup"><span data-stu-id="4053b-133">INPUTS</span></span>

### <span data-ttu-id="4053b-134">않아야</span><span class="sxs-lookup"><span data-stu-id="4053b-134">None</span></span>

## <span data-ttu-id="4053b-135">출력</span><span class="sxs-lookup"><span data-stu-id="4053b-135">OUTPUTS</span></span>

### <span data-ttu-id="4053b-136">목록\<IscsiConnection\></span><span class="sxs-lookup"><span data-stu-id="4053b-136">List\<IscsiConnection\></span></span>
<span data-ttu-id="4053b-137">이 cmdlet은 다음 속성을 포함 하는 iSCSI 연결 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="4053b-137">This cmdlet returns an iSCSI connection object that contains the following properties:</span></span> 

- <span data-ttu-id="4053b-138">**AcrInstanceId**</span><span class="sxs-lookup"><span data-stu-id="4053b-138">**AcrInstanceId**</span></span>
- <span data-ttu-id="4053b-139">**AcrName**</span><span class="sxs-lookup"><span data-stu-id="4053b-139">**AcrName**</span></span>
- <span data-ttu-id="4053b-140">**AllowedVolumeNames**</span><span class="sxs-lookup"><span data-stu-id="4053b-140">**AllowedVolumeNames**</span></span>
- <span data-ttu-id="4053b-141">**InitiatorAddress**</span><span class="sxs-lookup"><span data-stu-id="4053b-141">**InitiatorAddress**</span></span>
- <span data-ttu-id="4053b-142">**인터페이스**</span><span class="sxs-lookup"><span data-stu-id="4053b-142">**Interfaces**</span></span>
- <span data-ttu-id="4053b-143">**Iqn**</span><span class="sxs-lookup"><span data-stu-id="4053b-143">**Iqn**</span></span>
- <span data-ttu-id="4053b-144">**IscsiConnectionId**</span><span class="sxs-lookup"><span data-stu-id="4053b-144">**IscsiConnectionId**</span></span>

## <span data-ttu-id="4053b-145">상속자</span><span class="sxs-lookup"><span data-stu-id="4053b-145">NOTES</span></span>

## <span data-ttu-id="4053b-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4053b-146">RELATED LINKS</span></span>

[<span data-ttu-id="4053b-147">Get-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="4053b-147">Get-AzureStorSimpleAccessControlRecord</span></span>](./Get-AzureStorSimpleAccessControlRecord.md)


