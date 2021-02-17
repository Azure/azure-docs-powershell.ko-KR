---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: ED37B17D-C513-422A-89EA-A6AF1C9A5FEE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azcontainerserviceagentpoolprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzContainerServiceAgentPoolProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzContainerServiceAgentPoolProfile.md
ms.openlocfilehash: b887110ecb0cd941af9c91417218ec2ca297be1c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100210024"
---
# <span data-ttu-id="befb1-101">Remove-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="befb1-101">Remove-AzContainerServiceAgentPoolProfile</span></span>

## <span data-ttu-id="befb1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="befb1-102">SYNOPSIS</span></span>
<span data-ttu-id="befb1-103">컨테이너 서비스에서 에이전트 풀 프로필을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="befb1-103">Removes an agent pool profile from a container service.</span></span>

## <span data-ttu-id="befb1-104">구문</span><span class="sxs-lookup"><span data-stu-id="befb1-104">SYNTAX</span></span>

```
Remove-AzContainerServiceAgentPoolProfile [-ContainerService] <PSContainerService> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="befb1-105">설명</span><span class="sxs-lookup"><span data-stu-id="befb1-105">DESCRIPTION</span></span>
<span data-ttu-id="befb1-106">**Remove-AzContainerServiceAgentPoolProfile** cmdlet은 컨테이너 서비스에서 에이전트 풀 프로필을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="befb1-106">The **Remove-AzContainerServiceAgentPoolProfile** cmdlet removes an agent pool profile from a container service.</span></span>

## <span data-ttu-id="befb1-107">예제</span><span class="sxs-lookup"><span data-stu-id="befb1-107">EXAMPLES</span></span>

### <span data-ttu-id="befb1-108">예제 1: 컨테이너 서비스에서 프로필 제거</span><span class="sxs-lookup"><span data-stu-id="befb1-108">Example 1: Remove a profile from a container service</span></span>
```
PS C:\> $Container = Get-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" 
PS C:\> Remove-AzContainerServiceAgentPoolProfile -ContainerService $Container -Name "AgentPool01"
```

<span data-ttu-id="befb1-109">첫 번째 명령은 Get-AzContainerService cmdlet을 사용하여 CSResourceGroup17이라는 컨테이너 서비스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="befb1-109">The first command gets a container service named CSResourceGroup17 by using the Get-AzContainerService cmdlet.</span></span>
<span data-ttu-id="befb1-110">이 명령은 $Container 변수에 $Container 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="befb1-110">The command stores the service in the $Container variable.</span></span>
<span data-ttu-id="befb1-111">두 번째 명령은 에이전트Pool01이라는 프로필을 에이전트의 컨테이너 서비스에서 $Container.</span><span class="sxs-lookup"><span data-stu-id="befb1-111">The second command removes the profile named AgentPool01 from the container service in $Container.</span></span>

## <span data-ttu-id="befb1-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="befb1-112">PARAMETERS</span></span>

### <span data-ttu-id="befb1-113">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="befb1-113">-ContainerService</span></span>
<span data-ttu-id="befb1-114">이 cmdlet이 에이전트 풀 프로필을 제거하는 컨테이너 서비스 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="befb1-114">Specifies the container service object from which this cmdlet removes an agent pool profile.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="befb1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="befb1-115">-DefaultProfile</span></span>
<span data-ttu-id="befb1-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="befb1-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="befb1-117">-Name</span><span class="sxs-lookup"><span data-stu-id="befb1-117">-Name</span></span>
<span data-ttu-id="befb1-118">이 cmdlet이 제거하는 에이전트 풀 프로필의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="befb1-118">Specifies the name of the agent pool profile that this cmdlet removes.</span></span>

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

### <span data-ttu-id="befb1-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="befb1-119">-Confirm</span></span>
<span data-ttu-id="befb1-120">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="befb1-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="befb1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="befb1-121">-WhatIf</span></span>
<span data-ttu-id="befb1-122">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="befb1-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="befb1-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="befb1-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="befb1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="befb1-124">CommonParameters</span></span>
<span data-ttu-id="befb1-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="befb1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="befb1-126">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="befb1-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="befb1-127">입력</span><span class="sxs-lookup"><span data-stu-id="befb1-127">INPUTS</span></span>

### <span data-ttu-id="befb1-128">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span><span class="sxs-lookup"><span data-stu-id="befb1-128">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

### <span data-ttu-id="befb1-129">System.String</span><span class="sxs-lookup"><span data-stu-id="befb1-129">System.String</span></span>

## <span data-ttu-id="befb1-130">출력</span><span class="sxs-lookup"><span data-stu-id="befb1-130">OUTPUTS</span></span>

### <span data-ttu-id="befb1-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span><span class="sxs-lookup"><span data-stu-id="befb1-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="befb1-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="befb1-132">NOTES</span></span>

## <span data-ttu-id="befb1-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="befb1-133">RELATED LINKS</span></span>

[<span data-ttu-id="befb1-134">Add-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="befb1-134">Add-AzContainerServiceAgentPoolProfile</span></span>](./Add-AzContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="befb1-135">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="befb1-135">Get-AzContainerService</span></span>](./Get-AzContainerService.md)


