---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: C5A2A8D2-A840-4712-A8BD-F49C6063D193
online version: ''
schema: 2.0.0
ms.openlocfilehash: e1156b4887e7b97d4e783ec738a939d320fe397a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046292"
---
# <span data-ttu-id="892f2-101">Get-AzureStorSimpleDevice</span><span class="sxs-lookup"><span data-stu-id="892f2-101">Get-AzureStorSimpleDevice</span></span>

## <span data-ttu-id="892f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="892f2-102">SYNOPSIS</span></span>
<span data-ttu-id="892f2-103">리소스에 연결 된 장치를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="892f2-103">Gets devices attached to the resource.</span></span>

## <span data-ttu-id="892f2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="892f2-104">SYNTAX</span></span>

### <span data-ttu-id="892f2-105">비어 있음 (기본값)</span><span class="sxs-lookup"><span data-stu-id="892f2-105">Empty (Default)</span></span>
```
Get-AzureStorSimpleDevice [-Type <String>] [-ModelID <String>] [-Detailed] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="892f2-106">IdentifyById</span><span class="sxs-lookup"><span data-stu-id="892f2-106">IdentifyById</span></span>
```
Get-AzureStorSimpleDevice [-DeviceId <String>] [-Type <String>] [-ModelID <String>] [-Detailed]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="892f2-107">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="892f2-107">IdentifyByName</span></span>
```
Get-AzureStorSimpleDevice [-DeviceName <String>] [-Type <String>] [-ModelID <String>] [-Detailed]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="892f2-108">설명은</span><span class="sxs-lookup"><span data-stu-id="892f2-108">DESCRIPTION</span></span>
<span data-ttu-id="892f2-109">**Get-AzureStorSimpleDevice** cmdlet은 리소스에 연결 된 StorSimple 장치 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="892f2-109">The **Get-AzureStorSimpleDevice** cmdlet gets a list of StorSimple devices attached to the resource.</span></span>
<span data-ttu-id="892f2-110">장치 ID, 이름, 모델 ID 및 유형을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="892f2-110">You can specify device ID, name, model ID, and type.</span></span>
<span data-ttu-id="892f2-111">이 cmdlet을 사용 하 여 다른 StorSimple cmdlet에 대 한 디바이스를 지정 하 여 얻은 **DeviceID** 속성을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="892f2-111">Use the **DeviceID** property obtained by using this cmdlet to specify devices for other StorSimple cmdlets.</span></span>

## <span data-ttu-id="892f2-112">예제의</span><span class="sxs-lookup"><span data-stu-id="892f2-112">EXAMPLES</span></span>

### <span data-ttu-id="892f2-113">예제 1: 리소스에서 사용 가능한 디바이스 가져오기</span><span class="sxs-lookup"><span data-stu-id="892f2-113">Example 1: Get available devices on a resource</span></span>
```
PS C:\>Get-AzureStorSimpleDevice
DeviceId                  : 6f9ab151-39c7-4ded-b7d0-f5b0968f2766
DeviceName                : 8600-: SHX0881018G88
SerialNumber              : SHX0881018G88
DeviceSoftwareVersion     : 6.3.9600.17430
Location                  : 
ModelDescription          : 8600
Status                    : Offline
Type                      : Appliance
TargetIQN                 : iqn.1991-05.com.microsoft:storsimple8600-shx0991018g00e4-target
TimeZone                  : Pacific Standard Time
ActivationTime            : 2015-04-07T16:32:30.2960842Z
AvailableStorageInBytes   : 535363378479104
ProvisionedStorageInBytes : 14392435408896
TotalStorageInBytes       : 549755813888000
UsingStorageInBytes       : 12693995520

DeviceId                  : eb30ea31-c856-4cf2-9a02-aee611d6a3b9
DeviceName                : 8100-Delta 001
SerialNumber              : SHX90391XXXXXXX
DeviceSoftwareVersion     : 6.3.9600.17430
Location                  : 
ModelDescription          : 8100
Status                    : Online
Type                      : Appliance
TargetIQN                 : iqn.1991-05.com.microsoft:storsimple8100-shx90193xxxxxxx-target
TimeZone                  : Eastern Standard Time
ActivationTime            : 2015-03-26T14:53:14.4219391Z
AvailableStorageInBytes   : 205509890146304
ProvisionedStorageInBytes : 14392435408896
TotalStorageInBytes       : 219902325555200
UsingStorageInBytes       : 23904321536

DeviceId                  : edcb0b9b-1ed5-4102-9c5d-c589f7632994
DeviceName                : 8600-Bravo 001
SerialNumber              : SHX0900915G44SY
DeviceSoftwareVersion     : 6.3.9600.17430
Location                  : 
ModelDescription          : 8600
Status                    : Online
Type                      : Appliance
TargetIQN                 : iqn.1991-05.com.microsoft:storsimple8600-shx0900915g44sy-target
TimeZone                  : Eastern Standard Time
ActivationTime            : 2015-03-26T15:36:26.0870525Z
AvailableStorageInBytes   : 535363378479104
ProvisionedStorageInBytes : 14392435408896
TotalStorageInBytes       : 549755813888000
UsingStorageInBytes       : 978893799424
```

<span data-ttu-id="892f2-114">이 명령은 리소스에서 사용 가능한 모든 장치를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="892f2-114">This command gets all available devices on a resource.</span></span>
<span data-ttu-id="892f2-115">이 예제에서는 하나의 장치만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="892f2-115">In this example, only one device is available.</span></span>

### <span data-ttu-id="892f2-116">예제 2: 리소스에서 사용 가능한 특정 장치 가져오기</span><span class="sxs-lookup"><span data-stu-id="892f2-116">Example 2: Get specific available devices on a resource</span></span>
```
PS C:\>Get-AzureStorSimpleDevice -DeviceName "8600-SHX90193XXXXXXX" -Type Appliance -ModelId "8600"
DeviceId                  : f9db31da-8a6c-4718-8f5b-5ce89e600f28
DeviceName                : 8600-SHX90193XXXXXXX
SerialNumber              : SHX90193XXXXXXX
DeviceSoftwareVersion     : 6.3.9600.17430
Location                  : 
ModelDescription          : 8600
Status                    : Online
Type                      : Appliance
TargetIQN                 : iqn.1991-05.com.microsoft:storsimple8600-shx90193xxxxxxx-target
TimeZone                  : Pacific Standard Time
ActivationTime            : 2015-04-07T18:10:46.4524766Z
AvailableStorageInBytes   : 535363378479104
ProvisionedStorageInBytes : 14392435408896
TotalStorageInBytes       : 549755813888000
UsingStorageInBytes       : 14445182976
```

<span data-ttu-id="892f2-117">이 명령은 지정 된 이름, 유형 및 모델 ID가 있는 리소스에서 사용 가능한 모든 장치를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="892f2-117">This command gets all available devices on a resource that have the specified name, type, and model ID.</span></span>

### <span data-ttu-id="892f2-118">예제 3: 장치에 대 한 세부 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="892f2-118">Example 3: Get details for a device</span></span>
```
PS C:\>Get-AzureStorSimpleDevice -Name "8600-SHX90193XXXXXXX" -Type Appliance -Detailed
AlertNotification              : Microsoft.WindowsAzure.Management.StorSimple.Models.AlertNotificationSettings
Chap                           : Microsoft.WindowsAzure.Management.StorSimple.Models.ChapSettings
DeviceProperties               : Microsoft.WindowsAzure.Management.StorSimple.Models.DeviceInfo
DnsServer                      : Microsoft.WindowsAzure.Management.StorSimple.Models.DnsServerSettings
InstanceId                     : f9db31da-8a6c-4718-8f5b-5ce89e600f28
Name                           : 
NetInterfaceList               : {Data0, Data1, Data2, Data3...} 
OperationInProgress            : None
RemoteMgmtSettingsInfo         : Microsoft.WindowsAzure.Management.StorSimple.Models.RemoteManagementSettings

RemoteMinishellSecretInfo      : Microsoft.WindowsAzure.Management.StorSimple.Models.RemoteMinishellSettings
SecretEncryptionCertThumbprint : 
Snapshot                       : Microsoft.WindowsAzure.Management.StorSimple.Models.SnapshotSettings
TimeServer                     : Microsoft.WindowsAzure.Management.StorSimple.Models.TimeSettings
Type                           : Appliance
VirtualApplianceProperties     : Microsoft.WindowsAzure.Management.StorSimple.Models.VirtualApplianceInfo
WebProxy                       : Microsoft.WindowsAzure.Management.StorSimple.Models.WebProxySettings
```

<span data-ttu-id="892f2-119">이 명령은 지정 된 이름과 유형을 가진 리소스에서 사용 가능한 모든 장치를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="892f2-119">This command gets all available devices on a resource that have the specified name and type.</span></span>
<span data-ttu-id="892f2-120">이 명령은 *상세* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="892f2-120">This command specifies the *Detailed* parameter.</span></span>
<span data-ttu-id="892f2-121">명령은 반환 되는 장치에 대 한 추가 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="892f2-121">The command provides additional details about the devices it returns.</span></span>

## <span data-ttu-id="892f2-122">변수</span><span class="sxs-lookup"><span data-stu-id="892f2-122">PARAMETERS</span></span>

### <span data-ttu-id="892f2-123">-세부 정보</span><span class="sxs-lookup"><span data-stu-id="892f2-123">-Detailed</span></span>
<span data-ttu-id="892f2-124">이 cmdlet이 가져오는 장치에 대 한 디바이스 세부 정보를 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="892f2-124">Indicates that this cmdlet returns device details for the devices that it gets.</span></span>

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

### <span data-ttu-id="892f2-125">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="892f2-125">-DeviceId</span></span>
<span data-ttu-id="892f2-126">가져올 디바이스의 인스턴스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="892f2-126">Specifies the instance ID of the device to get.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: ID

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="892f2-127">-장치 이름</span><span class="sxs-lookup"><span data-stu-id="892f2-127">-DeviceName</span></span>
<span data-ttu-id="892f2-128">가져올 StorSimple 장치의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="892f2-128">Specifies the name of the StorSimple device to get.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="892f2-129">-ModelID</span><span class="sxs-lookup"><span data-stu-id="892f2-129">-ModelID</span></span>
<span data-ttu-id="892f2-130">가져올 StorSimple 장치 모델의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="892f2-130">Specifies the ID of the model of StorSimple devices to get.</span></span>

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

### <span data-ttu-id="892f2-131">-프로필</span><span class="sxs-lookup"><span data-stu-id="892f2-131">-Profile</span></span>
<span data-ttu-id="892f2-132">Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="892f2-132">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="892f2-133">-Type</span><span class="sxs-lookup"><span data-stu-id="892f2-133">-Type</span></span>
<span data-ttu-id="892f2-134">StorSimple 장치의 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="892f2-134">Specifies the type of a StorSimple device.</span></span>
<span data-ttu-id="892f2-135">유효한 값은 기기 및 VirtualAppliance입니다.</span><span class="sxs-lookup"><span data-stu-id="892f2-135">Valid values are: Appliance and VirtualAppliance.</span></span>

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

### <span data-ttu-id="892f2-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="892f2-136">CommonParameters</span></span>
<span data-ttu-id="892f2-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="892f2-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="892f2-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="892f2-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="892f2-139">입력</span><span class="sxs-lookup"><span data-stu-id="892f2-139">INPUTS</span></span>

### <span data-ttu-id="892f2-140">않아야</span><span class="sxs-lookup"><span data-stu-id="892f2-140">None</span></span>

## <span data-ttu-id="892f2-141">출력</span><span class="sxs-lookup"><span data-stu-id="892f2-141">OUTPUTS</span></span>

### <span data-ttu-id="892f2-142">List \<DeviceDetails\> , IEnumerable\<DeviceInfo\></span><span class="sxs-lookup"><span data-stu-id="892f2-142">List\<DeviceDetails\>, IEnumerable\<DeviceInfo\></span></span>
<span data-ttu-id="892f2-143">이 cmdlet은 *상세* 매개 변수를 지정 하는 경우 **목록 \<DeviceDetails\>** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="892f2-143">This cmdlet returns a **List\<DeviceDetails\>** object, if you specify the *Detailed* parameter.</span></span>
<span data-ttu-id="892f2-144">해당 매개 변수를 지정 하지 않으면 **IEnumerable \<DeviceInfo\>** 개체가 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="892f2-144">If you do not specify that parameter, it returns an **IEnumerable\<DeviceInfo\>** object.</span></span>

## <span data-ttu-id="892f2-145">상속자</span><span class="sxs-lookup"><span data-stu-id="892f2-145">NOTES</span></span>

## <span data-ttu-id="892f2-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="892f2-146">RELATED LINKS</span></span>

[<span data-ttu-id="892f2-147">Get-AzureStorSimpleResourceContext</span><span class="sxs-lookup"><span data-stu-id="892f2-147">Get-AzureStorSimpleResourceContext</span></span>](./Get-AzureStorSimpleResourceContext.md)

[<span data-ttu-id="892f2-148">선택-AzureStorSimpleResource</span><span class="sxs-lookup"><span data-stu-id="892f2-148">Select-AzureStorSimpleResource</span></span>](./Select-AzureStorSimpleResource.md)


