---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/invoke-azstackedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeDevice.md
ms.openlocfilehash: f25aeb501ff046a25330ad5db47bbdb06fbe7b35
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034507"
---
# <span data-ttu-id="d0bed-101">Invoke-AzStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="d0bed-101">Invoke-AzStackEdgeDevice</span></span>

## <span data-ttu-id="d0bed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0bed-102">SYNOPSIS</span></span>
<span data-ttu-id="d0bed-103">장치에서 특정 작업을 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0bed-103">Invokes specific actions on the device.</span></span>

## <span data-ttu-id="d0bed-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d0bed-104">SYNTAX</span></span>

### <span data-ttu-id="d0bed-105">InvokeScanForUpdateParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="d0bed-105">InvokeScanForUpdateParameterSet (Default)</span></span>
```
Invoke-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0bed-106">InvokeFetchUpdatesByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0bed-106">InvokeFetchUpdatesByResourceIdParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -ResourceId <String> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0bed-107">InvokeInstallUpdatesByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0bed-107">InvokeInstallUpdatesByResourceIdParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -ResourceId <String> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0bed-108">InvokeScanForUpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0bed-108">InvokeScanForUpdateByResourceIdParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -ResourceId <String> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0bed-109">InvokeInstallUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0bed-109">InvokeInstallUpdateParameterSet</span></span>
```
Invoke-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0bed-110">InvokeFetchUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0bed-110">InvokeFetchUpdateParameterSet</span></span>
```
Invoke-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0bed-111">InvokeFetchUpdatesByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0bed-111">InvokeFetchUpdatesByDeviceObjectParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -DeviceObject <PSStackEdgeDevice> [-FetchUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0bed-112">InvokeScanForUpdateByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0bed-112">InvokeScanForUpdateByDeviceObjectParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -DeviceObject <PSStackEdgeDevice> [-ScanForUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0bed-113">InvokeInstallUpdatesByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0bed-113">InvokeInstallUpdatesByDeviceObjectParameterSet</span></span>
```
Invoke-AzStackEdgeDevice -DeviceObject <PSStackEdgeDevice> [-InstallUpdate] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0bed-114">설명은</span><span class="sxs-lookup"><span data-stu-id="d0bed-114">DESCRIPTION</span></span>
<span data-ttu-id="d0bed-115">**AzStackEdgeDevice** Cmdlet은 스택 경계 장치에서 업데이트를 검색 하 고 다운로드 하 고 설치 하는 작업을 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0bed-115">The **Invoke-AzStackEdgeDevice** cmdlet invokes actions to scan, download �and install the updates on the Stack Edge device.</span></span> <span data-ttu-id="d0bed-116">장치에서 자동 스캔이 매일 실행 되며이 cmdlet을 실행 하 여 검사를 명시적으로 트리거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d0bed-116">An automatic scan runs on the device daily, you can trigger the scan explicitly by running this cmdlet.</span></span>

## <span data-ttu-id="d0bed-117">예제의</span><span class="sxs-lookup"><span data-stu-id="d0bed-117">EXAMPLES</span></span>

### <span data-ttu-id="d0bed-118">예제 1</span><span class="sxs-lookup"><span data-stu-id="d0bed-118">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -ScanForUpdate
```

### <span data-ttu-id="d0bed-119">예제 2</span><span class="sxs-lookup"><span data-stu-id="d0bed-119">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -FetchUpdate
```

### <span data-ttu-id="d0bed-120">예제 3</span><span class="sxs-lookup"><span data-stu-id="d0bed-120">Example 3</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -InstallUpdate
```

## <span data-ttu-id="d0bed-121">변수</span><span class="sxs-lookup"><span data-stu-id="d0bed-121">PARAMETERS</span></span>

### <span data-ttu-id="d0bed-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d0bed-122">-AsJob</span></span>
<span data-ttu-id="d0bed-123">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="d0bed-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d0bed-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0bed-124">-DefaultProfile</span></span>
<span data-ttu-id="d0bed-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d0bed-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0bed-126">DeviceObject</span><span class="sxs-lookup"><span data-stu-id="d0bed-126">-DeviceObject</span></span>
<span data-ttu-id="d0bed-127">해당 하는 디바이스 개체를 제공 하십시오.</span><span class="sxs-lookup"><span data-stu-id="d0bed-127">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="d0bed-128">-FetchUpdate</span><span class="sxs-lookup"><span data-stu-id="d0bed-128">-FetchUpdate</span></span>
<span data-ttu-id="d0bed-129">스택 edge/gateway 장치에서 업데이트를 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0bed-129">Downloads the updates on a Stack edge/gateway device</span></span>

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

### <span data-ttu-id="d0bed-130">-InstallUpdate</span><span class="sxs-lookup"><span data-stu-id="d0bed-130">-InstallUpdate</span></span>
<span data-ttu-id="d0bed-131">스택 가장자리/게이트웨이 장치에 업데이트를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0bed-131">Installs the updates on the Stack edge/gateway device</span></span>

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

### <span data-ttu-id="d0bed-132">-이름</span><span class="sxs-lookup"><span data-stu-id="d0bed-132">-Name</span></span>
<span data-ttu-id="d0bed-133">장치 이름</span><span class="sxs-lookup"><span data-stu-id="d0bed-133">Device Name</span></span>

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

### <span data-ttu-id="d0bed-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d0bed-134">-PassThru</span></span>
<span data-ttu-id="d0bed-135">성공한 경우 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0bed-135">returns true if successful</span></span>

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

### <span data-ttu-id="d0bed-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0bed-136">-ResourceGroupName</span></span>
<span data-ttu-id="d0bed-137">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="d0bed-137">Resource Group Name</span></span>

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

### <span data-ttu-id="d0bed-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d0bed-138">-ResourceId</span></span>
<span data-ttu-id="d0bed-139">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="d0bed-139">Azure ResourceId</span></span>

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

### <span data-ttu-id="d0bed-140">-ScanForUpdate</span><span class="sxs-lookup"><span data-stu-id="d0bed-140">-ScanForUpdate</span></span>
<span data-ttu-id="d0bed-141">스택 경계/게이트웨이 장치에서 업데이트를 검사 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0bed-141">Scans for updates on a Stack edge/gateway device.</span></span>

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

### <span data-ttu-id="d0bed-142">-확인</span><span class="sxs-lookup"><span data-stu-id="d0bed-142">-Confirm</span></span>
<span data-ttu-id="d0bed-143">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0bed-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0bed-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0bed-144">-WhatIf</span></span>
<span data-ttu-id="d0bed-145">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d0bed-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d0bed-146">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d0bed-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0bed-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0bed-147">CommonParameters</span></span>
<span data-ttu-id="d0bed-148">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0bed-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0bed-149">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d0bed-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0bed-150">입력</span><span class="sxs-lookup"><span data-stu-id="d0bed-150">INPUTS</span></span>

### <span data-ttu-id="d0bed-151">않아야</span><span class="sxs-lookup"><span data-stu-id="d0bed-151">None</span></span>

## <span data-ttu-id="d0bed-152">출력</span><span class="sxs-lookup"><span data-stu-id="d0bed-152">OUTPUTS</span></span>

### <span data-ttu-id="d0bed-153">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="d0bed-153">System.Boolean</span></span>

## <span data-ttu-id="d0bed-154">상속자</span><span class="sxs-lookup"><span data-stu-id="d0bed-154">NOTES</span></span>

## <span data-ttu-id="d0bed-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d0bed-155">RELATED LINKS</span></span>
