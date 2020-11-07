---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 38917534-49C6-47EA-B815-240F794EE655
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVM.md
ms.openlocfilehash: e87536a524766ac86b80d790ee1372336fedba17
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868829"
---
# <span data-ttu-id="00fac-101">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="00fac-101">Update-AzVM</span></span>

## <span data-ttu-id="00fac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00fac-102">SYNOPSIS</span></span>
<span data-ttu-id="00fac-103">Azure 가상 컴퓨터의 상태를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="00fac-103">Updates the state of an Azure virtual machine.</span></span>

## <span data-ttu-id="00fac-104">구문과</span><span class="sxs-lookup"><span data-stu-id="00fac-104">SYNTAX</span></span>

### <span data-ttu-id="00fac-105">ResourceGroupNameParameterSetName (기본값)</span><span class="sxs-lookup"><span data-stu-id="00fac-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 [-OsDiskWriteAccelerator <Boolean>] [-UltraSSDEnabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00fac-106">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="00fac-106">AssignIdentityParameterSet</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-AssignIdentity]
 [-OsDiskWriteAccelerator <Boolean>] [-UltraSSDEnabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00fac-107">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="00fac-107">ExplicitIdentityParameterSet</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="00fac-108">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="00fac-108">IdParameterSetName</span></span>
```
Update-AzVM [-Id] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="00fac-109">설명은</span><span class="sxs-lookup"><span data-stu-id="00fac-109">DESCRIPTION</span></span>
<span data-ttu-id="00fac-110">**업데이트 AzVM** Cmdlet은 Azure 가상 컴퓨터의 상태를 가상 컴퓨터 개체의 상태로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="00fac-110">The **Update-AzVM** cmdlet updates the state of an Azure virtual machine to the state of a virtual machine object.</span></span>

## <span data-ttu-id="00fac-111">예제의</span><span class="sxs-lookup"><span data-stu-id="00fac-111">EXAMPLES</span></span>

### <span data-ttu-id="00fac-112">예제 1: 가상 컴퓨터 업데이트</span><span class="sxs-lookup"><span data-stu-id="00fac-112">Example 1: Update a virtual machine</span></span>
```
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="00fac-113">이 명령은 ResourceGroup11에서 가상 머신 ($VirtualMachine)를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="00fac-113">This command updates the virtual machine, $VirtualMachine, in ResourceGroup11.</span></span>
<span data-ttu-id="00fac-114">이 명령은 $VirtualMachine 변수에 저장 된 가상 컴퓨터 개체를 사용 하 여 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="00fac-114">The command updates it by using the virtual machine object stored in the $VirtualMachine variable.</span></span>
<span data-ttu-id="00fac-115">가상 컴퓨터 개체를 가져오려면 **AzVM** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="00fac-115">To obtain a virtual machine object, use the **Get-AzVM** cmdlet.</span></span>

## <span data-ttu-id="00fac-116">변수</span><span class="sxs-lookup"><span data-stu-id="00fac-116">PARAMETERS</span></span>

### <span data-ttu-id="00fac-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="00fac-117">-AsJob</span></span>
<span data-ttu-id="00fac-118">백그라운드에서 cmdlet을 실행 하 고 작업을 반환 하 여 진행률을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="00fac-118">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="00fac-119">-Id 할당</span><span class="sxs-lookup"><span data-stu-id="00fac-119">-AssignIdentity</span></span>
<span data-ttu-id="00fac-120">가상 컴퓨터에 대해 시스템 할당 id를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="00fac-120">Specify the system-assigned identity for the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AssignIdentityParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00fac-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00fac-121">-DefaultProfile</span></span>
<span data-ttu-id="00fac-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="00fac-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00fac-123">-Id</span><span class="sxs-lookup"><span data-stu-id="00fac-123">-Id</span></span>
<span data-ttu-id="00fac-124">가상 컴퓨터의 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="00fac-124">Specifies the resource ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00fac-125">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="00fac-125">-IdentityId</span></span>
<span data-ttu-id="00fac-126">가상 컴퓨터와 연결 된 사용자 id 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="00fac-126">Specifies the list of user identities associated with the virtual machine.</span></span>
<span data-ttu-id="00fac-127">사용자 id 참조는 '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} ' 형식으로 팔로 리소스 Id를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="00fac-127">The user identity references will be ARM resource IDs in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: System.String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00fac-128">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="00fac-128">-IdentityType</span></span>
<span data-ttu-id="00fac-129">가상 컴퓨터에 사용 되는 id 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="00fac-129">The type of identity used for the virtual machine.</span></span> <span data-ttu-id="00fac-130">유효한 값은 SystemAssigned, UserAssigned, SystemAssignedUserAssigned 및 없음입니다.</span><span class="sxs-lookup"><span data-stu-id="00fac-130">Valid values are SystemAssigned, UserAssigned, SystemAssignedUserAssigned, and None.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00fac-131">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="00fac-131">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="00fac-132">OS 디스크에서 WriteAccelerator를 사용할지 아니면 disabled를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="00fac-132">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00fac-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00fac-133">-ResourceGroupName</span></span>
<span data-ttu-id="00fac-134">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="00fac-134">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName, AssignIdentityParameterSet, ExplicitIdentityParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00fac-135">태그</span><span class="sxs-lookup"><span data-stu-id="00fac-135">-Tag</span></span>
<span data-ttu-id="00fac-136">이름-값 쌍 집합을 사용 하 여 리소스 및 리소스 그룹에 태그를 지정할 수 있도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="00fac-136">Specifies the resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="00fac-137">리소스에 태그를 추가 하면 리소스 그룹에서 리소스를 그룹화 하 고 고유한 보기를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00fac-137">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="00fac-138">각 리소스 또는 리소스 그룹은 최대 15 개의 태그를 가질 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00fac-138">Each resource or resource group can have a maximum of 15 tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00fac-139">-UltraSSDEnabled</span><span class="sxs-lookup"><span data-stu-id="00fac-139">-UltraSSDEnabled</span></span>
<span data-ttu-id="00fac-140">VM에서 저장소 계정 유형이 UltraSSD_LRS 하나 이상의 관리 되는 데이터 디스크를 포함 하는 기능을 사용 하거나 사용 하지 않도록 설정 하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="00fac-140">The flag that enables or disables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="00fac-141">저장소 계정 유형이 UltraSSD_LRS 인 관리 디스크는이 속성을 사용 하도록 설정한 경우에만 가상 컴퓨터에 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00fac-141">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00fac-142">-VM</span><span class="sxs-lookup"><span data-stu-id="00fac-142">-VM</span></span>
<span data-ttu-id="00fac-143">로컬 가상 컴퓨터 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="00fac-143">Specifies a local virtual machine object.</span></span>
<span data-ttu-id="00fac-144">가상 컴퓨터 개체를 가져오려면 Get-AzVM cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="00fac-144">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="00fac-145">이 가상 컴퓨터 개체에는 가상 컴퓨터에 대 한 업데이트 상태가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="00fac-145">This virtual machine object contains the updated state for the virtual machine.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="00fac-146">-확인</span><span class="sxs-lookup"><span data-stu-id="00fac-146">-Confirm</span></span>
<span data-ttu-id="00fac-147">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="00fac-147">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00fac-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00fac-148">-WhatIf</span></span>
<span data-ttu-id="00fac-149">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="00fac-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00fac-150">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="00fac-150">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00fac-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00fac-151">CommonParameters</span></span>
<span data-ttu-id="00fac-152">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="00fac-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00fac-153">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00fac-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00fac-154">입력</span><span class="sxs-lookup"><span data-stu-id="00fac-154">INPUTS</span></span>

### <span data-ttu-id="00fac-155">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="00fac-155">System.String</span></span>

### <span data-ttu-id="00fac-156">PSVirtualMachine를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="00fac-156">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="00fac-157">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="00fac-157">System.Boolean</span></span>

## <span data-ttu-id="00fac-158">출력</span><span class="sxs-lookup"><span data-stu-id="00fac-158">OUTPUTS</span></span>

### <span data-ttu-id="00fac-159">이는 PSAzureOperationResponse를 계산 하는 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="00fac-159">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="00fac-160">상속자</span><span class="sxs-lookup"><span data-stu-id="00fac-160">NOTES</span></span>

## <span data-ttu-id="00fac-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="00fac-161">RELATED LINKS</span></span>

[<span data-ttu-id="00fac-162">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="00fac-162">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="00fac-163">새로운 AzVM</span><span class="sxs-lookup"><span data-stu-id="00fac-163">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="00fac-164">제거-AzVM</span><span class="sxs-lookup"><span data-stu-id="00fac-164">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="00fac-165">다시 시작-AzVM</span><span class="sxs-lookup"><span data-stu-id="00fac-165">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="00fac-166">시작-AzVM</span><span class="sxs-lookup"><span data-stu-id="00fac-166">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="00fac-167">중지-AzVM</span><span class="sxs-lookup"><span data-stu-id="00fac-167">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="00fac-168">새로운 AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="00fac-168">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


