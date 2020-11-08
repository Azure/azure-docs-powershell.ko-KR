---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 7EF20FC0-3E2A-4AFC-AC02-9B11C8952DB8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 22263501f2a79a36c1ace1915ee6898c4833b52b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045563"
---
# <span data-ttu-id="fe877-101">Get-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="fe877-101">Get-AzureStorSimpleDeviceVolumeContainer</span></span>

## <span data-ttu-id="fe877-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe877-102">SYNOPSIS</span></span>
<span data-ttu-id="fe877-103">장치에서 볼륨 컨테이너를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fe877-103">Gets volume containers on a device.</span></span>

## <span data-ttu-id="fe877-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fe877-104">SYNTAX</span></span>

```
Get-AzureStorSimpleDeviceVolumeContainer -DeviceName <String> [-VolumeContainerName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="fe877-105">설명은</span><span class="sxs-lookup"><span data-stu-id="fe877-105">DESCRIPTION</span></span>
<span data-ttu-id="fe877-106">**AzureStorSimpleDeviceVolumeContainer** cmdlet은 장치 또는 볼륨 컨테이너에서 지정 된 이름의 볼륨 컨테이너 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fe877-106">The **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet gets a list of volume containers on a device, or volume container that has the specified name.</span></span>
<span data-ttu-id="fe877-107">반환 된 개체에는 다음 속성이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fe877-107">The returned object contains the following properties:</span></span> 

- <span data-ttu-id="fe877-108">**BandwidthRate**</span><span class="sxs-lookup"><span data-stu-id="fe877-108">**BandwidthRate**</span></span>
- <span data-ttu-id="fe877-109">**Encryption.encryptionkey**</span><span class="sxs-lookup"><span data-stu-id="fe877-109">**EncryptionKey**</span></span>
- <span data-ttu-id="fe877-110">**InstanceId**</span><span class="sxs-lookup"><span data-stu-id="fe877-110">**InstanceId**</span></span>
- <span data-ttu-id="fe877-111">**IsDefault**</span><span class="sxs-lookup"><span data-stu-id="fe877-111">**IsDefault**</span></span>
- <span data-ttu-id="fe877-112">**Isa 사용**</span><span class="sxs-lookup"><span data-stu-id="fe877-112">**IsEncryptionEnabled**</span></span>
- <span data-ttu-id="fe877-113">**성을**</span><span class="sxs-lookup"><span data-stu-id="fe877-113">**Name**</span></span>
- <span data-ttu-id="fe877-114">**OperationInProgress**</span><span class="sxs-lookup"><span data-stu-id="fe877-114">**OperationInProgress**</span></span>
- <span data-ttu-id="fe877-115">**소유**</span><span class="sxs-lookup"><span data-stu-id="fe877-115">**Owned**</span></span>
- <span data-ttu-id="fe877-116">**PrimaryStorageAccountCredential**</span><span class="sxs-lookup"><span data-stu-id="fe877-116">**PrimaryStorageAccountCredential**</span></span>
- <span data-ttu-id="fe877-117">**SecretsEncryptionThumbprint**</span><span class="sxs-lookup"><span data-stu-id="fe877-117">**SecretsEncryptionThumbprint**</span></span>
- <span data-ttu-id="fe877-118">**(가) Ecount**</span><span class="sxs-lookup"><span data-stu-id="fe877-118">**VolumeCount**</span></span>

## <span data-ttu-id="fe877-119">예제의</span><span class="sxs-lookup"><span data-stu-id="fe877-119">EXAMPLES</span></span>

### <span data-ttu-id="fe877-120">예제 1: 장치에서 모든 컨테이너 가져오기</span><span class="sxs-lookup"><span data-stu-id="fe877-120">Example 1: Get all the containers on a device</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "8600-Bravo 001"
InstanceId                           Name                                             IsEncryptionEnabled  Owned BandwidthRate                                    PrimaryStorageAccountCredential                 VolumeCount                                    
----------                           ----                                             -------------------  ----- -------------                                    -------------------------------                 -----------                                    
127135b6-92de-4f53-850d-70e1f9a38cbe Test_Container                                   False                True  0                                                Test_Account                                    6
```

<span data-ttu-id="fe877-121">이 명령은 8600-Bravo 001 이라는 장치에서 볼륨 컨테이너의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fe877-121">This command gets a list of the volume containers on the device named 8600-Bravo 001.</span></span>

### <span data-ttu-id="fe877-122">예제 2: 이름을 사용 하 여 컨테이너 가져오기</span><span class="sxs-lookup"><span data-stu-id="fe877-122">Example 2: Get a container by using its name</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -VolumeContainerName "Container08"
VERBOSE: ClientRequestId: 8027c66a-869b-4ea3-97a2-e17d98ec751c_PS
VERBOSE: ClientRequestId: 344f9be5-0887-4d37-98ef-e45c557774f1_PS
VERBOSE: ClientRequestId: 14919be5-d6f5-4f81-b7f1-d7fafff2238c_PS


BandwidthRate                   : 256
EncryptionKey                   : 
InstanceId                      : 04ea9aad-7a56-4a50-b195-86061b0a810a
IsDefault                       : False
IsEncryptionEnabled             : False
Name                            : Container03
OperationInProgress             : None
Owned                           : True
PrimaryStorageAccountCredential : Microsoft.WindowsAzure.Management.StorSimple.Models.StorageAccountCredentialResponse
SecretsEncryptionThumbprint     : 
VolumeCount                     : 5

VERBOSE: Volume container with name: Container03 is found.
```

<span data-ttu-id="fe877-123">이 명령은 Contoso63-AppVm 이라는 장치에서 Container08 이라는 볼륨 컨테이너를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fe877-123">This command gets the volume container named Container08 on the device named Contoso63-AppVm.</span></span>

## <span data-ttu-id="fe877-124">변수</span><span class="sxs-lookup"><span data-stu-id="fe877-124">PARAMETERS</span></span>

### <span data-ttu-id="fe877-125">-장치 이름</span><span class="sxs-lookup"><span data-stu-id="fe877-125">-DeviceName</span></span>
<span data-ttu-id="fe877-126">StorSimple 장치의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe877-126">Specifies the name of a StorSimple device.</span></span>
<span data-ttu-id="fe877-127">이 cmdlet은이 매개 변수에서 지정 하는 장치에서 볼륨 컨테이너를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fe877-127">This cmdlet gets volume containers from the device that this parameter specifies.</span></span>

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

### <span data-ttu-id="fe877-128">-프로필</span><span class="sxs-lookup"><span data-stu-id="fe877-128">-Profile</span></span>
<span data-ttu-id="fe877-129">Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe877-129">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="fe877-130">-VolumeContainerName</span><span class="sxs-lookup"><span data-stu-id="fe877-130">-VolumeContainerName</span></span>
<span data-ttu-id="fe877-131">가져올 볼륨 컨테이너의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe877-131">Specifies the name of the volume container to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe877-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe877-132">CommonParameters</span></span>
<span data-ttu-id="fe877-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe877-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe877-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe877-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe877-135">입력</span><span class="sxs-lookup"><span data-stu-id="fe877-135">INPUTS</span></span>

### <span data-ttu-id="fe877-136">않아야</span><span class="sxs-lookup"><span data-stu-id="fe877-136">None</span></span>

## <span data-ttu-id="fe877-137">출력</span><span class="sxs-lookup"><span data-stu-id="fe877-137">OUTPUTS</span></span>

### <span data-ttu-id="fe877-138">DataContainer, IList\<DataContainer\></span><span class="sxs-lookup"><span data-stu-id="fe877-138">DataContainer, IList\<DataContainer\></span></span>
<span data-ttu-id="fe877-139">*VolumeContainerName* 매개 변수를 지정 하는 경우이 Cmdlet은 **DataContainer** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe877-139">This cmdlet returns a **DataContainer** object, if you specify the *VolumeContainerName* parameter.</span></span>
<span data-ttu-id="fe877-140">해당 매개 변수를 지정 하지 않으면이 cmdlet은 **IList \<DataContainer\>** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe877-140">If you do not specify that parameter, this cmdlet returns an **IList\<DataContainer\>** object.</span></span>

## <span data-ttu-id="fe877-141">상속자</span><span class="sxs-lookup"><span data-stu-id="fe877-141">NOTES</span></span>

## <span data-ttu-id="fe877-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fe877-142">RELATED LINKS</span></span>

[<span data-ttu-id="fe877-143">새로운 AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="fe877-143">New-AzureStorSimpleDeviceVolumeContainer</span></span>](./New-AzureStorSimpleDeviceVolumeContainer.md)

[<span data-ttu-id="fe877-144">제거-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="fe877-144">Remove-AzureStorSimpleDeviceVolumeContainer</span></span>](./Remove-AzureStorSimpleDeviceVolumeContainer.md)


