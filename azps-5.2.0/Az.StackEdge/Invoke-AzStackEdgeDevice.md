---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/invoke-azstackedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeDevice.md
ms.openlocfilehash: f25aeb501ff046a25330ad5db47bbdb06fbe7b35
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98344409"
---
# <span data-ttu-id="7dbde-101">Invoke-AzStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="7dbde-101">Invoke-AzStackEdgeDevice</span></span>

## <span data-ttu-id="7dbde-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7dbde-102">SYNOPSIS</span></span>
<span data-ttu-id="7dbde-103">디바이스에서 특정 작업을 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="7dbde-103">Invokes specific actions on the device.</span></span>

## <span data-ttu-id="7dbde-104">구문</span><span class="sxs-lookup"><span data-stu-id="7dbde-104">SYNTAX</span></span>

### <span data-ttu-id="7dbde-105">InvokeScanForUpdateParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="7dbde-105">InvokeScanForUpdateParameterSet (Default)</span></span>
```
Invoke-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7dbde-106">InvokeFetchUpdatesByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7dbde-106">InvokeFetchUpdatesByResourceIdParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -ResourceId <String> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7dbde-107">InvokeInstallUpdatesByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7dbde-107">InvokeInstallUpdatesByResourceIdParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -ResourceId <String> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7dbde-108">InvokeScanForUpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7dbde-108">InvokeScanForUpdateByResourceIdParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -ResourceId <String> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7dbde-109">InvokeInstallUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="7dbde-109">InvokeInstallUpdateParameterSet</span></span>
```
Invoke-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7dbde-110">InvokeFetchUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="7dbde-110">InvokeFetchUpdateParameterSet</span></span>
```
Invoke-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7dbde-111">InvokeFetchUpdatesByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7dbde-111">InvokeFetchUpdatesByDeviceObjectParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -DeviceObject <PSStackEdgeDevice> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7dbde-112">InvokeScanForUpdateByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7dbde-112">InvokeScanForUpdateByDeviceObjectParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -DeviceObject <PSStackEdgeDevice> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7dbde-113">InvokeInstallUpdatesByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7dbde-113">InvokeInstallUpdatesByDeviceObjectParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -DeviceObject <PSStackEdgeDevice> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7dbde-114">설명</span><span class="sxs-lookup"><span data-stu-id="7dbde-114">DESCRIPTION</span></span>
<span data-ttu-id="7dbde-115">**Invoke-AzStackEdgeDevice** cmdlet은 Stack Edge 디바이스에서 업데이트를 검색, 다운로드 및 설치하는 작업을 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="7dbde-115">The **Invoke-AzStackEdgeDevice** cmdlet invokes actions to scan, download �and install the updates on the Stack Edge device.</span></span> <span data-ttu-id="7dbde-116">자동 검사는 디바이스에서 매일 실행됩니다. 이 cmdlet을 실행하여 명시적으로 검색을 트리거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7dbde-116">An automatic scan runs on the device daily, you can trigger the scan explicitly by running this cmdlet.</span></span>

## <span data-ttu-id="7dbde-117">예제</span><span class="sxs-lookup"><span data-stu-id="7dbde-117">EXAMPLES</span></span>

### <span data-ttu-id="7dbde-118">예제 1</span><span class="sxs-lookup"><span data-stu-id="7dbde-118">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -ScanForUpdate
```

### <span data-ttu-id="7dbde-119">예제 2</span><span class="sxs-lookup"><span data-stu-id="7dbde-119">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -FetchUpdate
```

### <span data-ttu-id="7dbde-120">예제 3</span><span class="sxs-lookup"><span data-stu-id="7dbde-120">Example 3</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -InstallUpdate
```

## <span data-ttu-id="7dbde-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7dbde-121">PARAMETERS</span></span>

### <span data-ttu-id="7dbde-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7dbde-122">-AsJob</span></span>
<span data-ttu-id="7dbde-123">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="7dbde-123">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7dbde-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7dbde-124">-DefaultProfile</span></span>
<span data-ttu-id="7dbde-125">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7dbde-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7dbde-126">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="7dbde-126">-DeviceObject</span></span>
<span data-ttu-id="7dbde-127">해당 디바이스 개체를 제공하세요.</span><span class="sxs-lookup"><span data-stu-id="7dbde-127">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice
Parameter Sets: InvokeFetchUpdatesByDeviceObjectParameterSet, InvokeScanForUpdateByDeviceObjectParameterSet, InvokeInstallUpdatesByDeviceObjectParameterSet
Aliases: Device

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7dbde-128">-FetchUpdate</span><span class="sxs-lookup"><span data-stu-id="7dbde-128">-FetchUpdate</span></span>
<span data-ttu-id="7dbde-129">스택 에지/게이트웨이 디바이스에서 업데이트를 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="7dbde-129">Downloads the updates on a Stack edge/gateway device</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: InvokeFetchUpdatesByResourceIdParameterSet, InvokeFetchUpdateParameterSet, InvokeFetchUpdatesByDeviceObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7dbde-130">-InstallUpdate</span><span class="sxs-lookup"><span data-stu-id="7dbde-130">-InstallUpdate</span></span>
<span data-ttu-id="7dbde-131">스택 에지/게이트웨이 디바이스에 업데이트를 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="7dbde-131">Installs the updates on the Stack edge/gateway device</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: InvokeInstallUpdatesByResourceIdParameterSet, InvokeInstallUpdateParameterSet, InvokeInstallUpdatesByDeviceObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7dbde-132">-Name</span><span class="sxs-lookup"><span data-stu-id="7dbde-132">-Name</span></span>
<span data-ttu-id="7dbde-133">디바이스 이름</span><span class="sxs-lookup"><span data-stu-id="7dbde-133">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeScanForUpdateParameterSet, InvokeInstallUpdateParameterSet, InvokeFetchUpdateParameterSet
Aliases: DeviceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7dbde-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7dbde-134">-PassThru</span></span>
<span data-ttu-id="7dbde-135">성공한 경우 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="7dbde-135">returns true if successful</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7dbde-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7dbde-136">-ResourceGroupName</span></span>
<span data-ttu-id="7dbde-137">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="7dbde-137">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeScanForUpdateParameterSet, InvokeInstallUpdateParameterSet, InvokeFetchUpdateParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7dbde-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7dbde-138">-ResourceId</span></span>
<span data-ttu-id="7dbde-139">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="7dbde-139">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeFetchUpdatesByResourceIdParameterSet, InvokeInstallUpdatesByResourceIdParameterSet, InvokeScanForUpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7dbde-140">-ScanForUpdate</span><span class="sxs-lookup"><span data-stu-id="7dbde-140">-ScanForUpdate</span></span>
<span data-ttu-id="7dbde-141">스택 에지/게이트웨이 디바이스에서 업데이트를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="7dbde-141">Scans for updates on a Stack edge/gateway device.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: InvokeScanForUpdateParameterSet, InvokeScanForUpdateByResourceIdParameterSet, InvokeScanForUpdateByDeviceObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7dbde-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7dbde-142">-Confirm</span></span>
<span data-ttu-id="7dbde-143">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7dbde-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7dbde-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7dbde-144">-WhatIf</span></span>
<span data-ttu-id="7dbde-145">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="7dbde-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7dbde-146">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7dbde-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7dbde-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7dbde-147">CommonParameters</span></span>
<span data-ttu-id="7dbde-148">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7dbde-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7dbde-149">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7dbde-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7dbde-150">입력</span><span class="sxs-lookup"><span data-stu-id="7dbde-150">INPUTS</span></span>

### <span data-ttu-id="7dbde-151">없음</span><span class="sxs-lookup"><span data-stu-id="7dbde-151">None</span></span>

## <span data-ttu-id="7dbde-152">출력</span><span class="sxs-lookup"><span data-stu-id="7dbde-152">OUTPUTS</span></span>

### <span data-ttu-id="7dbde-153">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7dbde-153">System.Boolean</span></span>

## <span data-ttu-id="7dbde-154">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7dbde-154">NOTES</span></span>

## <span data-ttu-id="7dbde-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7dbde-155">RELATED LINKS</span></span>
