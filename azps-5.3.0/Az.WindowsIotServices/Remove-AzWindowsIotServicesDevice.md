---
external help file: ''
Module Name: Az.WindowsIotServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.windowsiotservices/remove-azwindowsiotservicesdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Remove-AzWindowsIotServicesDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Remove-AzWindowsIotServicesDevice.md
ms.openlocfilehash: 265c0e68dd3f19afbefd8cf993e058f56e3ec9f3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491364"
---
# <span data-ttu-id="7ddc8-101">Remove-AzWindowsIotServicesDevice</span><span class="sxs-lookup"><span data-stu-id="7ddc8-101">Remove-AzWindowsIotServicesDevice</span></span>

## <span data-ttu-id="7ddc8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ddc8-102">SYNOPSIS</span></span>
<span data-ttu-id="7ddc8-103">Windows IoT 디바이스 서비스를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="7ddc8-103">Delete a Windows IoT Device Service.</span></span>

## <span data-ttu-id="7ddc8-104">구문</span><span class="sxs-lookup"><span data-stu-id="7ddc8-104">SYNTAX</span></span>

### <span data-ttu-id="7ddc8-105">삭제(기본값)</span><span class="sxs-lookup"><span data-stu-id="7ddc8-105">Delete (Default)</span></span>
```
Remove-AzWindowsIotServicesDevice -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7ddc8-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7ddc8-106">DeleteViaIdentity</span></span>
```
Remove-AzWindowsIotServicesDevice -InputObject <IWindowsIotServicesIdentity> [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7ddc8-107">설명</span><span class="sxs-lookup"><span data-stu-id="7ddc8-107">DESCRIPTION</span></span>
<span data-ttu-id="7ddc8-108">Windows IoT 디바이스 서비스를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="7ddc8-108">Delete a Windows IoT Device Service.</span></span>

## <span data-ttu-id="7ddc8-109">예제</span><span class="sxs-lookup"><span data-stu-id="7ddc8-109">EXAMPLES</span></span>

### <span data-ttu-id="7ddc8-110">예제 1: 이름으로 Windows IoT 서비스 제거</span><span class="sxs-lookup"><span data-stu-id="7ddc8-110">Example 1: Remove a Windows IoT services by name</span></span>
```powershell
PS C:\> Remove-AzWindowsIotServicesDevice -Name wsi-t03 -ResourceGroupName azure-rg-test

```

<span data-ttu-id="7ddc8-111">이 명령은 이름으로 Windows IoT 서비스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7ddc8-111">This command removes a Windows IoT services by name.</span></span>

### <span data-ttu-id="7ddc8-112">예제 2: 파이프라인으로 Windows IoT 서비스 제거</span><span class="sxs-lookup"><span data-stu-id="7ddc8-112">Example 2: Remove a Windows IoT services by pipeline</span></span>
```powershell
PS C:\> Get-AzWindowsIotServicesDevice -ResourceGroupName azure-rg-test -Name wsi-t01 | Remove-AzWindowsIotServicesDevice


```

<span data-ttu-id="7ddc8-113">이 명령은 파이프라인에 의해 Windows IoT 서비스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7ddc8-113">This command removes a Windows IoT services by pipeline.</span></span>

## <span data-ttu-id="7ddc8-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7ddc8-114">PARAMETERS</span></span>

### <span data-ttu-id="7ddc8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ddc8-115">-DefaultProfile</span></span>
<span data-ttu-id="7ddc8-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7ddc8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ddc8-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7ddc8-117">-InputObject</span></span>
<span data-ttu-id="7ddc8-118">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="7ddc8-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7ddc8-119">-Name</span><span class="sxs-lookup"><span data-stu-id="7ddc8-119">-Name</span></span>
<span data-ttu-id="7ddc8-120">Windows IoT 디바이스 서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7ddc8-120">The name of the Windows IoT Device Service.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ddc8-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ddc8-121">-ResourceGroupName</span></span>
<span data-ttu-id="7ddc8-122">Windows IoT Device Service를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7ddc8-122">The name of the resource group that contains the Windows IoT Device Service.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ddc8-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7ddc8-123">-SubscriptionId</span></span>
<span data-ttu-id="7ddc8-124">구독 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="7ddc8-124">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ddc8-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7ddc8-125">-Confirm</span></span>
<span data-ttu-id="7ddc8-126">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7ddc8-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ddc8-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ddc8-127">-WhatIf</span></span>
<span data-ttu-id="7ddc8-128">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="7ddc8-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ddc8-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7ddc8-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ddc8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ddc8-130">CommonParameters</span></span>
<span data-ttu-id="7ddc8-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7ddc8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ddc8-132">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7ddc8-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ddc8-133">입력</span><span class="sxs-lookup"><span data-stu-id="7ddc8-133">INPUTS</span></span>

### <span data-ttu-id="7ddc8-134">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity</span><span class="sxs-lookup"><span data-stu-id="7ddc8-134">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity</span></span>

## <span data-ttu-id="7ddc8-135">출력</span><span class="sxs-lookup"><span data-stu-id="7ddc8-135">OUTPUTS</span></span>

### <span data-ttu-id="7ddc8-136">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span><span class="sxs-lookup"><span data-stu-id="7ddc8-136">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span></span>

## <span data-ttu-id="7ddc8-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7ddc8-137">NOTES</span></span>

<span data-ttu-id="7ddc8-138">별칭</span><span class="sxs-lookup"><span data-stu-id="7ddc8-138">ALIASES</span></span>

<span data-ttu-id="7ddc8-139">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="7ddc8-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7ddc8-140">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="7ddc8-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7ddc8-141">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7ddc8-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7ddc8-142">INPUTOBJECT: <IWindowsIotServicesIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="7ddc8-142">INPUTOBJECT <IWindowsIotServicesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7ddc8-143">`[DeviceName <String>]`: Windows IoT 디바이스 서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7ddc8-143">`[DeviceName <String>]`: The name of the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="7ddc8-144">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="7ddc8-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7ddc8-145">`[ResourceGroupName <String>]`: Windows IoT 디바이스 서비스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7ddc8-145">`[ResourceGroupName <String>]`: The name of the resource group that contains the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="7ddc8-146">`[SubscriptionId <String>]`: 구독 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="7ddc8-146">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="7ddc8-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7ddc8-147">RELATED LINKS</span></span>

