---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 43D01A97-75B9-46CE-B007-26FE6A97C31C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzContainerService.md
ms.openlocfilehash: 199b61bc8ef075aabc09870cde436a0e49598ee8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372429"
---
# <span data-ttu-id="53106-101">Update-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="53106-101">Update-AzContainerService</span></span>

## <span data-ttu-id="53106-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53106-102">SYNOPSIS</span></span>
<span data-ttu-id="53106-103">컨테이너 서비스의 상태를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="53106-103">Updates the state of a container service.</span></span>

## <span data-ttu-id="53106-104">구문</span><span class="sxs-lookup"><span data-stu-id="53106-104">SYNTAX</span></span>

```
Update-AzContainerService [-ResourceGroupName] <String> [-Name] <String>
 [-ContainerService] <PSContainerService> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53106-105">설명</span><span class="sxs-lookup"><span data-stu-id="53106-105">DESCRIPTION</span></span>
<span data-ttu-id="53106-106">**Update-AzContainerService** cmdlet은 서비스의 로컬 인스턴스와 일치하게 컨테이너 서비스의 상태를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="53106-106">The **Update-AzContainerService** cmdlet updates the state of a container service to match a local instance of the service.</span></span>

## <span data-ttu-id="53106-107">예제</span><span class="sxs-lookup"><span data-stu-id="53106-107">EXAMPLES</span></span>

### <span data-ttu-id="53106-108">예제 1: 컨테이너 서비스 업데이트</span><span class="sxs-lookup"><span data-stu-id="53106-108">Example 1: Update a container service</span></span>
```
PS C:\> Get-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" | Remove-AzContainerServiceAgentPoolProfile -Name "AgentPool01" | Add-AzContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17" -Count 2 | Update-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="53106-109">이 명령은 Get-AzContainerService cmdlet을 사용하여 CSResourceGroup17이라는 컨테이너 서비스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="53106-109">This command gets the container service named CSResourceGroup17 by using the Get-AzContainerService cmdlet.</span></span>
<span data-ttu-id="53106-110">이 명령은 파이프라인 연산자를 사용하여 Remove-AzContainerServiceAgentPoolProfile cmdlet에 해당 개체를 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="53106-110">The command passes that object to the Remove-AzContainerServiceAgentPoolProfile cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="53106-111">**Remove-AzContainerServiceAgentPoolProfile은** AgentPool01이라는 프로필을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="53106-111">**Remove-AzContainerServiceAgentPoolProfile** removes the profile named AgentPool01.</span></span>
<span data-ttu-id="53106-112">명령은 결과를 Add-AzContainerServiceAgentPoolProfile cmdlet에 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="53106-112">The command passes the result to the Add-AzContainerServiceAgentPoolProfile cmdlet.</span></span>
<span data-ttu-id="53106-113">**Add-AzContainerServiceAgentPoolProfile은** AgentPool01 이름이 있으며 지정된 속성이 있는 프로필을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="53106-113">**Add-AzContainerServiceAgentPoolProfile** adds a profile that has the name AgentPool01, and has the specified properties.</span></span>
<span data-ttu-id="53106-114">이 명령은 결과를 현재 cmdlet에 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="53106-114">The command passes the result to the current cmdlet.</span></span>
<span data-ttu-id="53106-115">현재 cmdlet은 이 명령에서 변경된 내용을 반영하기 위해 컨테이너 서비스를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="53106-115">The current cmdlet updates the container service to reflect the changes that were made in this command.</span></span>

## <span data-ttu-id="53106-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="53106-116">PARAMETERS</span></span>

### <span data-ttu-id="53106-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="53106-117">-AsJob</span></span>
<span data-ttu-id="53106-118">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="53106-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="53106-119">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="53106-119">-ContainerService</span></span>
<span data-ttu-id="53106-120">변경 내용을 포함하는 로컬 **ContainerService** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="53106-120">Specifies a local **ContainerService** object that contains changes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="53106-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53106-121">-DefaultProfile</span></span>
<span data-ttu-id="53106-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="53106-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53106-123">-Name</span><span class="sxs-lookup"><span data-stu-id="53106-123">-Name</span></span>
<span data-ttu-id="53106-124">이 cmdlet이 업데이트하는 컨테이너 서비스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="53106-124">Specifies the name of the container service that this cmdlet updates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53106-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53106-125">-ResourceGroupName</span></span>
<span data-ttu-id="53106-126">이 cmdlet이 업데이트하는 컨테이너 서비스의 리소스 그룹을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="53106-126">Specifies the resource group of the container service that this cmdlet updates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53106-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="53106-127">-Confirm</span></span>
<span data-ttu-id="53106-128">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="53106-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53106-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53106-129">-WhatIf</span></span>
<span data-ttu-id="53106-130">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="53106-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53106-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="53106-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53106-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53106-132">CommonParameters</span></span>
<span data-ttu-id="53106-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="53106-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53106-134">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="53106-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53106-135">입력</span><span class="sxs-lookup"><span data-stu-id="53106-135">INPUTS</span></span>

### <span data-ttu-id="53106-136">System.String</span><span class="sxs-lookup"><span data-stu-id="53106-136">System.String</span></span>

### <span data-ttu-id="53106-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span><span class="sxs-lookup"><span data-stu-id="53106-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="53106-138">출력</span><span class="sxs-lookup"><span data-stu-id="53106-138">OUTPUTS</span></span>

### <span data-ttu-id="53106-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span><span class="sxs-lookup"><span data-stu-id="53106-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="53106-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="53106-140">NOTES</span></span>

## <span data-ttu-id="53106-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="53106-141">RELATED LINKS</span></span>

[<span data-ttu-id="53106-142">Add-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="53106-142">Add-AzContainerServiceAgentPoolProfile</span></span>](./Add-AzContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="53106-143">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="53106-143">Get-AzContainerService</span></span>](./Get-AzContainerService.md)

[<span data-ttu-id="53106-144">New-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="53106-144">New-AzContainerService</span></span>](./New-AzContainerService.md)

[<span data-ttu-id="53106-145">Remove-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="53106-145">Remove-AzContainerService</span></span>](./Remove-AzContainerService.md)

[<span data-ttu-id="53106-146">Remove-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="53106-146">Remove-AzContainerServiceAgentPoolProfile</span></span>](./Remove-AzContainerServiceAgentPoolProfile.md)


