---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: CE1C6576-234E-4891-9158-FA45B64B786C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 41e8641b01dcb95a6b6939ff3551fe03b642ddf0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045435"
---
# <span data-ttu-id="9c845-101">Set-AzureStorSimpleVirtualDevice</span><span class="sxs-lookup"><span data-stu-id="9c845-101">Set-AzureStorSimpleVirtualDevice</span></span>

## <span data-ttu-id="9c845-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c845-102">SYNOPSIS</span></span>
<span data-ttu-id="9c845-103">StorSimple 가상 장치의 장치 구성을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c845-103">Creates or updates the device configuration of a StorSimple virtual device.</span></span>

## <span data-ttu-id="9c845-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9c845-104">SYNTAX</span></span>

```
Set-AzureStorSimpleVirtualDevice -DeviceName <String> -SecretKey <String> -AdministratorPassword <String>
 -SnapshotManagerPassword <String> [-TimeZone <TimeZoneInfo>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9c845-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9c845-105">DESCRIPTION</span></span>
<span data-ttu-id="9c845-106">**AzureStorSimpleVirtualDevice** Cmdlet은 Azure StorSimple 가상 장치의 장치 구성을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c845-106">The **Set-AzureStorSimpleVirtualDevice** cmdlet creates or updates the device configuration of an Azure StorSimple virtual device.</span></span>

## <span data-ttu-id="9c845-107">예제의</span><span class="sxs-lookup"><span data-stu-id="9c845-107">EXAMPLES</span></span>

### <span data-ttu-id="9c845-108">예제 1: 가상 장치 업데이트</span><span class="sxs-lookup"><span data-stu-id="9c845-108">Example 1: Update a virtual device</span></span>
```
PS C:\>$TimeZoneInfo = [System.TimeZoneInfo]::GetSystemTimeZones() | where { $_.Id -eq "Pacific Standard Time" }
PS C:\> Set-AzureStorSimpleVirtualDevice -DeviceName "Contoso23" -SecretKey "wcZBlBGpCMf4USdSKyt/SQ==" -TimeZone $TimeZoneInfo
VERBOSE: ClientRequestId: e31f0d6b-451d-4c1d-b2f1-3fc84c13972c_PS
VERBOSE: ClientRequestId: df58db83-d563-4a2e-bbb4-9576f0e69ca6_PS
VERBOSE: ClientRequestId: 494a9f0d-79ee-4fde-ab4d-85ee5a357556_PS
VERBOSE: ClientRequestId: ce557cbf-174d-4301-93d4-5ffe082c8413_PS
VERBOSE: ClientRequestId: 31284dad-de2c-4758-a2ef-45962875bfa6_PS
VERBOSE: About to configure the device : win-ff93i74m1e1 ! 
VERBOSE: ClientRequestId: d9c66302-45d8-488a-adda-8ccf957f77d3_PS


TaskId       : 21f530c3-bc47-4591-8c4e-da4d694b751d
TaskResult   : Succeeded
TaskStatus   : Completed
ErrorCode    : 
ErrorMessage : 
TaskSteps    : {Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep, Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep}

VERBOSE: The task created for your Setup operation has completed successfully. 
VERBOSE: ClientRequestId: a94f972c-18ea-40b6-9401-2ad209c0c8b4_PS
AlertNotification              : Microsoft.WindowsAzure.Management.StorSimple.Models.AlertNotificationSettings
Chap                           : Microsoft.WindowsAzure.Management.StorSimple.Models.ChapSettings
DeviceProperties               : Microsoft.WindowsAzure.Management.StorSimple.Models.DeviceInfo
DnsServer                      : Microsoft.WindowsAzure.Management.StorSimple.Models.DnsServerSettings
InstanceId                     : d369ebb4-8b9a-47fc-9a6b-60f371e123ae
Name                           : 
NetInterfaceList               : {}
OperationInProgress            : None
RemoteMgmtSettingsInfo         : Microsoft.WindowsAzure.Management.StorSimple.Models.RemoteManagementSettings
RemoteMinishellSecretInfo      : Microsoft.WindowsAzure.Management.StorSimple.Models.RemoteMinishellSettings
SecretEncryptionCertThumbprint : 
Snapshot                       : Microsoft.WindowsAzure.Management.StorSimple.Models.SnapshotSettings
TimeServer                     : Microsoft.WindowsAzure.Management.StorSimple.Models.TimeSettings
Type                           : VirtualAppliance
VirtualApplianceProperties     : Microsoft.WindowsAzure.Management.StorSimple.Models.VirtualApplianceInfo
WebProxy                       : Microsoft.WindowsAzure.Management.StorSimple.Models.WebProxySettings

VERBOSE: Successfully updated configuration for device Contoso23 with id d369ebb4-8b9a-47fc-9a6b-60f371e123ae
```

<span data-ttu-id="9c845-109">첫 번째 명령은 **TimeZoneInfo** .net 클래스와 표준 구문을 사용 하 여 태평양 표준 시간대를 가져오고 해당 개체를 $TimeZoneInfo 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c845-109">The first command uses the **System.TimeZoneInfo** .NET class and standard syntax to get Pacific Standard Time zone, and stores that object in the $TimeZoneInfo variable.</span></span>

<span data-ttu-id="9c845-110">두 번째 명령은 Contoso23 이라는 장치를 업데이트 하 여 $TimeZoneInfo에 지정 된 표준 시간대를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c845-110">The second command updates the device named Contoso23 to use the time zone specified in $TimeZoneInfo.</span></span>
<span data-ttu-id="9c845-111">명령에 가상 장치 구성에 액세스 하려면 비밀 키가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c845-111">The command requires the secret key to access the virtual device configuration.</span></span>

### <span data-ttu-id="9c845-112">예제 2: 파이프라인 연산자를 사용 하 여 가상 장치 업데이트</span><span class="sxs-lookup"><span data-stu-id="9c845-112">Example 2: Update a virtual device by using the pipeline operator</span></span>
```
PS C:\> [System.TimeZoneInfo]::GetSystemTimeZones() | where { $_.Id -eq "Pacific Standard Time" } | Set-AzureStorSimpleVirtualDevice -DeviceName "Contoso23" -SecretKey "wcZBlBGpCMf4USdSKyt/SQ=="
```

<span data-ttu-id="9c845-113">이 명령은 Contoso23 이라는 장치를 업데이트 하 여 명령이 만드는 표준 시간대를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c845-113">This command updates the device named Contoso23 to use the time zone that the command creates.</span></span>
<span data-ttu-id="9c845-114">명령에 가상 장치 구성에 액세스 하려면 비밀 키가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c845-114">The command requires the secret key to access the virtual device configuration.</span></span>
<span data-ttu-id="9c845-115">이 명령은 파이프라인 연산자를 사용 하 여 현재 cmdlet에 표준 시간대를 전달 한다는 점을 제외 하 고 이전 예제와 동일한 방식으로 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c845-115">This command works the same way as the previous example, except that it passes the time zone to the current cmdlet by using the pipeline operator.</span></span>

## <span data-ttu-id="9c845-116">변수</span><span class="sxs-lookup"><span data-stu-id="9c845-116">PARAMETERS</span></span>

### <span data-ttu-id="9c845-117">-관리자 암호</span><span class="sxs-lookup"><span data-stu-id="9c845-117">-AdministratorPassword</span></span>
<span data-ttu-id="9c845-118">구성할 가상 디바이스의 관리자 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c845-118">Specifies the administrator password of the virtual device to configure.</span></span>

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

### <span data-ttu-id="9c845-119">-장치 이름</span><span class="sxs-lookup"><span data-stu-id="9c845-119">-DeviceName</span></span>
<span data-ttu-id="9c845-120">구성할 가상 디바이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c845-120">Specifies the name of the virtual device to configure.</span></span>

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

### <span data-ttu-id="9c845-121">-프로필</span><span class="sxs-lookup"><span data-stu-id="9c845-121">-Profile</span></span>
<span data-ttu-id="9c845-122">Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c845-122">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="9c845-123">-SecretKey</span><span class="sxs-lookup"><span data-stu-id="9c845-123">-SecretKey</span></span>
<span data-ttu-id="9c845-124">가상 장치에 대 한 서비스 암호화 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c845-124">Specifies a service encryption key for the virtual device.</span></span>
<span data-ttu-id="9c845-125">이 키는 첫 번째 물리적 장치가 리소스에 등록 되어 있는 경우에 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9c845-125">This key is generated when the first physical device is registered with a resource.</span></span>

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

### <span data-ttu-id="9c845-126">-SnapshotManagerPassword</span><span class="sxs-lookup"><span data-stu-id="9c845-126">-SnapshotManagerPassword</span></span>
<span data-ttu-id="9c845-127">스냅숏 관리자 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c845-127">Specifies the snapshot manager password.</span></span>

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

### <span data-ttu-id="9c845-128">-표준 시간대</span><span class="sxs-lookup"><span data-stu-id="9c845-128">-TimeZone</span></span>
<span data-ttu-id="9c845-129">장치에 대 한 표준 시간대를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c845-129">Specifies a time zone for the device.</span></span>
<span data-ttu-id="9c845-130">**Getsystemtimezone ()** 메서드를 사용 하 여 **TimeZoneInfo** 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9c845-130">You can create a **TimeZoneInfo** object by using the **GetSystemTimeZone()** method.</span></span>
<span data-ttu-id="9c845-131">예를 들어이 명령은 태평양 표준시에 대 한 표준 시간대 정보 개체를 만듭니다. `\[System.TimeZoneInfo\]::GetSystemTimeZones() | where { $_.Id -eq "Pacific Standard Time" }`</span><span class="sxs-lookup"><span data-stu-id="9c845-131">For example, this command creates a time zone information object for Pacific Standard Time: `\[System.TimeZoneInfo\]::GetSystemTimeZones() | where { $_.Id -eq "Pacific Standard Time" }`</span></span>

```yaml
Type: TimeZoneInfo
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9c845-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c845-132">CommonParameters</span></span>
<span data-ttu-id="9c845-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c845-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c845-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c845-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c845-135">입력</span><span class="sxs-lookup"><span data-stu-id="9c845-135">INPUTS</span></span>

### <span data-ttu-id="9c845-136">TimeZoneInfo</span><span class="sxs-lookup"><span data-stu-id="9c845-136">TimeZoneInfo</span></span>
<span data-ttu-id="9c845-137">**TimeZoneInfo** 개체를이 cmdlet에 파이프 하 여 연결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9c845-137">You can pipe a **TimeZoneInfo** object to this cmdlet.</span></span>

## <span data-ttu-id="9c845-138">출력</span><span class="sxs-lookup"><span data-stu-id="9c845-138">OUTPUTS</span></span>

### <span data-ttu-id="9c845-139">DeviceJobDetails</span><span class="sxs-lookup"><span data-stu-id="9c845-139">DeviceJobDetails</span></span>
<span data-ttu-id="9c845-140">이 cmdlet은 가상 장치에 대 한 업데이트 된 장치 세부 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c845-140">This cmdlet returns updated device details for the virtual device.</span></span>

## <span data-ttu-id="9c845-141">상속자</span><span class="sxs-lookup"><span data-stu-id="9c845-141">NOTES</span></span>

## <span data-ttu-id="9c845-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9c845-142">RELATED LINKS</span></span>

[<span data-ttu-id="9c845-143">새로운 AzureStorSimpleVirtualDevice</span><span class="sxs-lookup"><span data-stu-id="9c845-143">New-AzureStorSimpleVirtualDevice</span></span>](./New-AzureStorSimpleVirtualDevice.md)

[<span data-ttu-id="9c845-144">Set-AzureStorSimpleDevice</span><span class="sxs-lookup"><span data-stu-id="9c845-144">Set-AzureStorSimpleDevice</span></span>](./Set-AzureStorSimpleDevice.md)


