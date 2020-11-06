---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 38917534-49C6-47EA-B815-240F794EE655
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmVM.md
ms.openlocfilehash: ad337c07f22b2805002347758f91bf0ea781adad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531828"
---
# <span data-ttu-id="c15c8-101">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="c15c8-101">Update-AzureRmVM</span></span>

## <span data-ttu-id="c15c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c15c8-102">SYNOPSIS</span></span>
<span data-ttu-id="c15c8-103">Azure 가상 컴퓨터의 상태를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c15c8-103">Updates the state of an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c15c8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c15c8-104">SYNTAX</span></span>

### <span data-ttu-id="c15c8-105">ResourceGroupNameParameterSetName (기본값)</span><span class="sxs-lookup"><span data-stu-id="c15c8-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Update-AzureRmVM -VM <PSVirtualMachine> [-Tags <Hashtable>] [-IdentityType <ResourceIdentityType>]
 [-AssignIdentity] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c15c8-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="c15c8-106">IdParameterSetName</span></span>
```
Update-AzureRmVM -VM <PSVirtualMachine> [-Tags <Hashtable>] [-IdentityType <ResourceIdentityType>]
 [-AssignIdentity] [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c15c8-107">설명은</span><span class="sxs-lookup"><span data-stu-id="c15c8-107">DESCRIPTION</span></span>
<span data-ttu-id="c15c8-108">**업데이트 AzureRmVM** Cmdlet은 Azure 가상 컴퓨터의 상태를 가상 컴퓨터 개체의 상태로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c15c8-108">The **Update-AzureRmVM** cmdlet updates the state of an Azure virtual machine to the state of a virtual machine object.</span></span>

## <span data-ttu-id="c15c8-109">예제의</span><span class="sxs-lookup"><span data-stu-id="c15c8-109">EXAMPLES</span></span>

### <span data-ttu-id="c15c8-110">예제 1: 가상 컴퓨터 업데이트</span><span class="sxs-lookup"><span data-stu-id="c15c8-110">Example 1: Update a virtual machine</span></span>
```
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="c15c8-111">이 명령은 ResourceGroup11에서 가상 머신 ($VirtualMachine)를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c15c8-111">This command updates the virtual machine, $VirtualMachine, in ResourceGroup11.</span></span>
<span data-ttu-id="c15c8-112">이 명령은 $VirtualMachine 변수에 저장 된 가상 컴퓨터 개체를 사용 하 여 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c15c8-112">The command updates it by using the virtual machine object stored in the $VirtualMachine variable.</span></span>
<span data-ttu-id="c15c8-113">가상 컴퓨터 개체를 가져오려면 **AzureRmVM** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c15c8-113">To obtain a virtual machine object, use the **Get-AzureRmVM** cmdlet.</span></span>

## <span data-ttu-id="c15c8-114">변수</span><span class="sxs-lookup"><span data-stu-id="c15c8-114">PARAMETERS</span></span>

### <span data-ttu-id="c15c8-115">-Id 할당</span><span class="sxs-lookup"><span data-stu-id="c15c8-115">-AssignIdentity</span></span>
<span data-ttu-id="c15c8-116">시스템에서 가상 컴퓨터용으로 할당 된 id를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c15c8-116">Specify the system assigned identity for the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c15c8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c15c8-117">-DefaultProfile</span></span>
<span data-ttu-id="c15c8-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c15c8-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c15c8-119">-Id</span><span class="sxs-lookup"><span data-stu-id="c15c8-119">-Id</span></span>
<span data-ttu-id="c15c8-120">가상 컴퓨터의 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c15c8-120">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="c15c8-121">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="c15c8-121">-IdentityType</span></span>
<span data-ttu-id="c15c8-122">가상 컴퓨터에 사용 되는 id 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="c15c8-122">The type of identity used for the virtual machine.</span></span> <span data-ttu-id="c15c8-123">현재는 암시적으로 id를 만드는 ' SystemAssigned ' 형식이 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c15c8-123">Currently, the only supported type is 'SystemAssigned', which implicitly creates an identity.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: (All)
Aliases: 
Accepted values: SystemAssigned

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c15c8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c15c8-124">-ResourceGroupName</span></span>
<span data-ttu-id="c15c8-125">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c15c8-125">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c15c8-126">태그</span><span class="sxs-lookup"><span data-stu-id="c15c8-126">-Tags</span></span>
<span data-ttu-id="c15c8-127">이름-값 쌍 집합을 사용 하 여 리소스 및 리소스 그룹에 태그를 지정할 수 있도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c15c8-127">Specifies the resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="c15c8-128">리소스에 태그를 추가 하면 리소스 그룹에서 리소스를 그룹화 하 고 고유한 보기를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c15c8-128">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="c15c8-129">각 리소스 또는 리소스 그룹은 최대 15 개의 태그를 가질 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c15c8-129">Each resource or resource group can have a maximum of 15 tags.</span></span>

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

### <span data-ttu-id="c15c8-130">-VM</span><span class="sxs-lookup"><span data-stu-id="c15c8-130">-VM</span></span>
<span data-ttu-id="c15c8-131">로컬 가상 컴퓨터 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c15c8-131">Specifies a local virtual machine object.</span></span>
<span data-ttu-id="c15c8-132">가상 컴퓨터 개체를 가져오려면 Get-AzureRmVM cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c15c8-132">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>
<span data-ttu-id="c15c8-133">이 가상 컴퓨터 개체에는 가상 컴퓨터에 대 한 업데이트 상태가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c15c8-133">This virtual machine object contains the updated state for the virtual machine.</span></span>

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

### <span data-ttu-id="c15c8-134">-확인</span><span class="sxs-lookup"><span data-stu-id="c15c8-134">-Confirm</span></span>
<span data-ttu-id="c15c8-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c15c8-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c15c8-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c15c8-136">-WhatIf</span></span>
<span data-ttu-id="c15c8-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c15c8-137">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="c15c8-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c15c8-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c15c8-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c15c8-139">CommonParameters</span></span>
<span data-ttu-id="c15c8-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c15c8-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c15c8-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c15c8-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c15c8-142">입력</span><span class="sxs-lookup"><span data-stu-id="c15c8-142">INPUTS</span></span>

## <span data-ttu-id="c15c8-143">출력</span><span class="sxs-lookup"><span data-stu-id="c15c8-143">OUTPUTS</span></span>

## <span data-ttu-id="c15c8-144">상속자</span><span class="sxs-lookup"><span data-stu-id="c15c8-144">NOTES</span></span>

## <span data-ttu-id="c15c8-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c15c8-145">RELATED LINKS</span></span>

[<span data-ttu-id="c15c8-146">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="c15c8-146">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="c15c8-147">새로운 AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="c15c8-147">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="c15c8-148">제거-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="c15c8-148">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="c15c8-149">다시 시작-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="c15c8-149">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="c15c8-150">시작-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="c15c8-150">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="c15c8-151">중지-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="c15c8-151">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="c15c8-152">새로운 AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="c15c8-152">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)


