---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 38917534-49C6-47EA-B815-240F794EE655
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmVM.md
ms.openlocfilehash: e29eb849dfd7ec3417daaea1b0cae447d20f1322
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532067"
---
# <span data-ttu-id="eca79-101">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="eca79-101">Update-AzureRmVM</span></span>

## <span data-ttu-id="eca79-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eca79-102">SYNOPSIS</span></span>
<span data-ttu-id="eca79-103">Azure 가상 컴퓨터의 상태를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="eca79-103">Updates the state of an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eca79-104">구문과</span><span class="sxs-lookup"><span data-stu-id="eca79-104">SYNTAX</span></span>

### <span data-ttu-id="eca79-105">ResourceGroupNameParameterSetName (기본값)</span><span class="sxs-lookup"><span data-stu-id="eca79-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Update-AzureRmVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 [-OsDiskWriteAccelerator <Boolean>] [-UltraSSDEnabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eca79-106">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="eca79-106">AssignIdentityParameterSet</span></span>
```
Update-AzureRmVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-AssignIdentity]
 [-OsDiskWriteAccelerator <Boolean>] [-UltraSSDEnabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eca79-107">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="eca79-107">ExplicitIdentityParameterSet</span></span>
```
Update-AzureRmVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="eca79-108">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="eca79-108">IdParameterSetName</span></span>
```
Update-AzureRmVM [-Id] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eca79-109">설명은</span><span class="sxs-lookup"><span data-stu-id="eca79-109">DESCRIPTION</span></span>
<span data-ttu-id="eca79-110">**업데이트 AzureRmVM** Cmdlet은 Azure 가상 컴퓨터의 상태를 가상 컴퓨터 개체의 상태로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="eca79-110">The **Update-AzureRmVM** cmdlet updates the state of an Azure virtual machine to the state of a virtual machine object.</span></span>

## <span data-ttu-id="eca79-111">예제의</span><span class="sxs-lookup"><span data-stu-id="eca79-111">EXAMPLES</span></span>

### <span data-ttu-id="eca79-112">예제 1: 가상 컴퓨터 업데이트</span><span class="sxs-lookup"><span data-stu-id="eca79-112">Example 1: Update a virtual machine</span></span>
```
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="eca79-113">이 명령은 ResourceGroup11에서 가상 머신 ($VirtualMachine)를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="eca79-113">This command updates the virtual machine, $VirtualMachine, in ResourceGroup11.</span></span>
<span data-ttu-id="eca79-114">이 명령은 $VirtualMachine 변수에 저장 된 가상 컴퓨터 개체를 사용 하 여 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="eca79-114">The command updates it by using the virtual machine object stored in the $VirtualMachine variable.</span></span>
<span data-ttu-id="eca79-115">가상 컴퓨터 개체를 가져오려면 **AzureRmVM** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="eca79-115">To obtain a virtual machine object, use the **Get-AzureRmVM** cmdlet.</span></span>

## <span data-ttu-id="eca79-116">변수</span><span class="sxs-lookup"><span data-stu-id="eca79-116">PARAMETERS</span></span>

### <span data-ttu-id="eca79-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eca79-117">-AsJob</span></span>
<span data-ttu-id="eca79-118">백그라운드에서 cmdlet을 실행 하 고 작업을 반환 하 여 진행률을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="eca79-118">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="eca79-119">-Id 할당</span><span class="sxs-lookup"><span data-stu-id="eca79-119">-AssignIdentity</span></span>
<span data-ttu-id="eca79-120">시스템에서 가상 컴퓨터용으로 할당 된 id를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eca79-120">Specify the system assigned identity for the virtual machine.</span></span>

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

### <span data-ttu-id="eca79-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eca79-121">-DefaultProfile</span></span>
<span data-ttu-id="eca79-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="eca79-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eca79-123">-Id</span><span class="sxs-lookup"><span data-stu-id="eca79-123">-Id</span></span>
<span data-ttu-id="eca79-124">가상 컴퓨터의 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eca79-124">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="eca79-125">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="eca79-125">-IdentityId</span></span>
<span data-ttu-id="eca79-126">가상 컴퓨터 배율 집합과 연결 된 사용자 id 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eca79-126">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="eca79-127">사용자 id 참조는 '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} ' 형식으로 팔로 리소스 id를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="eca79-127">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="eca79-128">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="eca79-128">-IdentityType</span></span>
<span data-ttu-id="eca79-129">가상 컴퓨터에 사용 되는 id 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="eca79-129">The type of identity used for the virtual machine.</span></span> <span data-ttu-id="eca79-130">현재는 암시적으로 id를 만드는 ' SystemAssigned ' 형식이 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="eca79-130">Currently, the only supported type is 'SystemAssigned', which implicitly creates an identity.</span></span>

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

### <span data-ttu-id="eca79-131">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="eca79-131">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="eca79-132">OS 디스크에서 WriteAccelerator를 사용할지 아니면 disabled를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eca79-132">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="eca79-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eca79-133">-ResourceGroupName</span></span>
<span data-ttu-id="eca79-134">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eca79-134">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="eca79-135">태그</span><span class="sxs-lookup"><span data-stu-id="eca79-135">-Tag</span></span>
<span data-ttu-id="eca79-136">이름-값 쌍 집합을 사용 하 여 리소스 및 리소스 그룹에 태그를 지정할 수 있도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eca79-136">Specifies the resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="eca79-137">리소스에 태그를 추가 하면 리소스 그룹에서 리소스를 그룹화 하 고 고유한 보기를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eca79-137">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="eca79-138">각 리소스 또는 리소스 그룹은 최대 15 개의 태그를 가질 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eca79-138">Each resource or resource group can have a maximum of 15 tags.</span></span>

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

### <span data-ttu-id="eca79-139">-UltraSSDEnabled</span><span class="sxs-lookup"><span data-stu-id="eca79-139">-UltraSSDEnabled</span></span>
<span data-ttu-id="eca79-140">VM에서 저장소 계정 유형이 UltraSSD_LRS 하나 이상의 관리 되는 데이터 디스크를 포함 하는 기능을 사용 하거나 사용 하지 않도록 설정 하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="eca79-140">The flag that enables or disables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="eca79-141">저장소 계정 유형이 UltraSSD_LRS 인 관리 디스크는이 속성을 사용 하도록 설정한 경우에만 가상 컴퓨터에 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eca79-141">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>

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

### <span data-ttu-id="eca79-142">-VM</span><span class="sxs-lookup"><span data-stu-id="eca79-142">-VM</span></span>
<span data-ttu-id="eca79-143">로컬 가상 컴퓨터 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eca79-143">Specifies a local virtual machine object.</span></span>
<span data-ttu-id="eca79-144">가상 컴퓨터 개체를 가져오려면 Get-AzureRmVM cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="eca79-144">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>
<span data-ttu-id="eca79-145">이 가상 컴퓨터 개체에는 가상 컴퓨터에 대 한 업데이트 상태가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="eca79-145">This virtual machine object contains the updated state for the virtual machine.</span></span>

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

### <span data-ttu-id="eca79-146">-확인</span><span class="sxs-lookup"><span data-stu-id="eca79-146">-Confirm</span></span>
<span data-ttu-id="eca79-147">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="eca79-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eca79-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eca79-148">-WhatIf</span></span>
<span data-ttu-id="eca79-149">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="eca79-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eca79-150">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eca79-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eca79-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eca79-151">CommonParameters</span></span>
<span data-ttu-id="eca79-152">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="eca79-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eca79-153">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eca79-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eca79-154">입력</span><span class="sxs-lookup"><span data-stu-id="eca79-154">INPUTS</span></span>

### <span data-ttu-id="eca79-155">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="eca79-155">System.String</span></span>

### <span data-ttu-id="eca79-156">PSVirtualMachine를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="eca79-156">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="eca79-157">출력</span><span class="sxs-lookup"><span data-stu-id="eca79-157">OUTPUTS</span></span>

### <span data-ttu-id="eca79-158">이는 PSAzureOperationResponse를 계산 하는 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="eca79-158">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="eca79-159">상속자</span><span class="sxs-lookup"><span data-stu-id="eca79-159">NOTES</span></span>

## <span data-ttu-id="eca79-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="eca79-160">RELATED LINKS</span></span>

[<span data-ttu-id="eca79-161">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="eca79-161">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="eca79-162">새로운 AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="eca79-162">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="eca79-163">제거-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="eca79-163">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="eca79-164">다시 시작-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="eca79-164">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="eca79-165">시작-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="eca79-165">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="eca79-166">중지-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="eca79-166">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="eca79-167">새로운 AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="eca79-167">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)


