---
external help file: ''
Module Name: Az.WindowsIotServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.windowsiotservices/get-azwindowsiotservicesdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Get-AzWindowsIotServicesDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Get-AzWindowsIotServicesDevice.md
ms.openlocfilehash: b9236dc7c3e4a12c9be6b72cd63874044ee49065
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98347270"
---
# <span data-ttu-id="47429-101">Get-AzWindowsIotServicesDevice</span><span class="sxs-lookup"><span data-stu-id="47429-101">Get-AzWindowsIotServicesDevice</span></span>

## <span data-ttu-id="47429-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47429-102">SYNOPSIS</span></span>
<span data-ttu-id="47429-103">Windows IoT 디바이스 서비스의 비보안 관련 메타데이터를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="47429-103">Get the non-security related metadata of a Windows IoT Device Service.</span></span>

## <span data-ttu-id="47429-104">구문</span><span class="sxs-lookup"><span data-stu-id="47429-104">SYNTAX</span></span>

### <span data-ttu-id="47429-105">List1(기본값)</span><span class="sxs-lookup"><span data-stu-id="47429-105">List1 (Default)</span></span>
```
Get-AzWindowsIotServicesDevice [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="47429-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="47429-106">Get</span></span>
```
Get-AzWindowsIotServicesDevice -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="47429-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="47429-107">GetViaIdentity</span></span>
```
Get-AzWindowsIotServicesDevice -InputObject <IWindowsIotServicesIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="47429-108">목록</span><span class="sxs-lookup"><span data-stu-id="47429-108">List</span></span>
```
Get-AzWindowsIotServicesDevice -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="47429-109">설명</span><span class="sxs-lookup"><span data-stu-id="47429-109">DESCRIPTION</span></span>
<span data-ttu-id="47429-110">Windows IoT 디바이스 서비스의 비보안 관련 메타데이터를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="47429-110">Get the non-security related metadata of a Windows IoT Device Service.</span></span>

## <span data-ttu-id="47429-111">예제</span><span class="sxs-lookup"><span data-stu-id="47429-111">EXAMPLES</span></span>

### <span data-ttu-id="47429-112">예제 1: 구독에서 모든 Windows IoT 서비스 다운로드</span><span class="sxs-lookup"><span data-stu-id="47429-112">Example 1: Get all Windows IoT services under a subscription</span></span>
```powershell
PS C:\> Get-AzWindowsIotServicesDevice

Location Name    Type                                Etag
-------- ----    ----                                ----
West US  wsi-t01 Microsoft.WindowsIoT/DeviceServices "5c006e63-0000-0700-0000-5faa37830000"
eastus   wsi-t02 Microsoft.WindowsIoT/DeviceServices "5c006ad2-0000-0700-0000-5faa3e090000"
```

<span data-ttu-id="47429-113">이 명령은 구독에서 모든 Windows IoT 서비스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="47429-113">This command gets all Windows IoT services under a subscription.</span></span>

### <span data-ttu-id="47429-114">예제 2: 리소스 그룹에서 모든 Windows IoT 서비스 다운로드</span><span class="sxs-lookup"><span data-stu-id="47429-114">Example 2: Get all Windows IoT services under a resource group</span></span>
```powershell
PS C:\> Get-AzWindowsIotServicesDevice -ResourceGroupName azure-rg-test

Location Name    Type                                Etag
-------- ----    ----                                ----
West US  wsi-t01 Microsoft.WindowsIoT/DeviceServices "5c006e63-0000-0700-0000-5faa37830000"
eastus   wsi-t02 Microsoft.WindowsIoT/DeviceServices "5c006ad2-0000-0700-0000-5faa3e090000"
```

<span data-ttu-id="47429-115">이 명령은 리소스 그룹에서 모든 Windows IoT 서비스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="47429-115">This command gets all Windows IoT services under a resource group.</span></span>

### <span data-ttu-id="47429-116">예제 3: 이름으로 Windows IoT 서비스 다운로드</span><span class="sxs-lookup"><span data-stu-id="47429-116">Example 3: Get a Windows IoT service by name</span></span>
```powershell
PS C:\> Get-AzWindowsIotServicesDevice -ResourceGroupName azure-rg-test -Name wsi-t01

Location Name    Type                                Etag
-------- ----    ----                                ----
West US  wsi-t01 Microsoft.WindowsIoT/DeviceServices "5c006e63-0000-0700-0000-5faa37830000"
```

<span data-ttu-id="47429-117">이 명령은 이름으로 Windows IoT 서비스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="47429-117">This command gets a Windows IoT service by name.</span></span>

### <span data-ttu-id="47429-118">예제 4: 개체로 Windows IoT 서비스 다운로드</span><span class="sxs-lookup"><span data-stu-id="47429-118">Example 4: Get a Windows IoT service by object</span></span>
```powershell
PS C:\> $wsi = New-AzWindowsIotServicesDevice -Name wsi-t01 -ResourceGroupName azure-rg-test -Location eastus -Quantity 10 -BillingDomainName 'microsoft.onmicrosoft.com' -AdminDomainName 'microsoft.onmicrosoft.com'
PS C:\> Get-AzWindowsIotServicesDevice -InputObject $wsi

Location Name    Type                                Etag
-------- ----    ----                                ----
West US  wsi-t01 Microsoft.WindowsIoT/DeviceServices "5c006e63-0000-0700-0000-5faa37830000"
```

<span data-ttu-id="47429-119">이 명령은 개체로 Windows IoT 서비스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="47429-119">This command gets a Windows IoT service by object.</span></span>

### <span data-ttu-id="47429-120">예제 4: 파이프라인으로 Windows IoT 서비스 다운로드</span><span class="sxs-lookup"><span data-stu-id="47429-120">Example 4: Get a Windows IoT service by pipeline</span></span>
```powershell
PS C:\> $wsi = New-AzWindowsIotServicesDevice -Name wsi-t01 -ResourceGroupName azure-rg-test -Location eastus -Quantity 10 -BillingDomainName 'microsoft.onmicrosoft.com' -AdminDomainName 'microsoft.onmicrosoft.com' | Get-AzWindowsIotServicesDevice

Location Name    Type                                Etag
-------- ----    ----                                ----
West US  wsi-t01 Microsoft.WindowsIoT/DeviceServices "5c006e63-0000-0700-0000-5faa37830000"
```

<span data-ttu-id="47429-121">이 명령은 파이프라인에 의해 Windows IoT 서비스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="47429-121">This command gets a Windows IoT service by pipeline.</span></span>

## <span data-ttu-id="47429-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="47429-122">PARAMETERS</span></span>

### <span data-ttu-id="47429-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47429-123">-DefaultProfile</span></span>
<span data-ttu-id="47429-124">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="47429-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47429-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="47429-125">-InputObject</span></span>
<span data-ttu-id="47429-126">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="47429-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="47429-127">-Name</span><span class="sxs-lookup"><span data-stu-id="47429-127">-Name</span></span>
<span data-ttu-id="47429-128">Windows IoT 디바이스 서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="47429-128">The name of the Windows IoT Device Service.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47429-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47429-129">-ResourceGroupName</span></span>
<span data-ttu-id="47429-130">Windows IoT Device Service를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="47429-130">The name of the resource group that contains the Windows IoT Device Service.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47429-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="47429-131">-SubscriptionId</span></span>
<span data-ttu-id="47429-132">구독 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="47429-132">The subscription identifier.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47429-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47429-133">CommonParameters</span></span>
<span data-ttu-id="47429-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="47429-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47429-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="47429-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47429-136">입력</span><span class="sxs-lookup"><span data-stu-id="47429-136">INPUTS</span></span>

### <span data-ttu-id="47429-137">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity</span><span class="sxs-lookup"><span data-stu-id="47429-137">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity</span></span>

## <span data-ttu-id="47429-138">출력</span><span class="sxs-lookup"><span data-stu-id="47429-138">OUTPUTS</span></span>

### <span data-ttu-id="47429-139">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span><span class="sxs-lookup"><span data-stu-id="47429-139">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span></span>

## <span data-ttu-id="47429-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="47429-140">NOTES</span></span>

<span data-ttu-id="47429-141">별칭</span><span class="sxs-lookup"><span data-stu-id="47429-141">ALIASES</span></span>

<span data-ttu-id="47429-142">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="47429-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="47429-143">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="47429-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="47429-144">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="47429-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="47429-145">INPUTOBJECT: <IWindowsIotServicesIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="47429-145">INPUTOBJECT <IWindowsIotServicesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="47429-146">`[DeviceName <String>]`: Windows IoT 디바이스 서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="47429-146">`[DeviceName <String>]`: The name of the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="47429-147">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="47429-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="47429-148">`[ResourceGroupName <String>]`: Windows IoT 디바이스 서비스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="47429-148">`[ResourceGroupName <String>]`: The name of the resource group that contains the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="47429-149">`[SubscriptionId <String>]`: 구독 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="47429-149">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="47429-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="47429-150">RELATED LINKS</span></span>

