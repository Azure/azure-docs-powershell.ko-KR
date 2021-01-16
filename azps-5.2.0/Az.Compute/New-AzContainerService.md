---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 522F5305-CDF6-41F2-803B-9EEA9E927668
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzContainerService.md
ms.openlocfilehash: e401755786c8f1aaf967417f526c8a976b333048
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98349209"
---
# <span data-ttu-id="f83b4-101">New-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="f83b4-101">New-AzContainerService</span></span>

## <span data-ttu-id="f83b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f83b4-102">SYNOPSIS</span></span>
<span data-ttu-id="f83b4-103">컨테이너 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f83b4-103">Creates a container service.</span></span>

## <span data-ttu-id="f83b4-104">구문</span><span class="sxs-lookup"><span data-stu-id="f83b4-104">SYNTAX</span></span>

```
New-AzContainerService [-ResourceGroupName] <String> [-Name] <String> [-ContainerService] <PSContainerService>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f83b4-105">설명</span><span class="sxs-lookup"><span data-stu-id="f83b4-105">DESCRIPTION</span></span>
<span data-ttu-id="f83b4-106">**New-AzContainerService** cmdlet은 컨테이너 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f83b4-106">The **New-AzContainerService** cmdlet creates a container service.</span></span>
<span data-ttu-id="f83b4-107">New-AzContainerServiceConfig cmdlet을 사용하여 만들 수 있는 컨테이너 서비스 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f83b4-107">Specify a container service object that you can create by using the New-AzContainerServiceConfig cmdlet.</span></span>

## <span data-ttu-id="f83b4-108">예제</span><span class="sxs-lookup"><span data-stu-id="f83b4-108">EXAMPLES</span></span>

### <span data-ttu-id="f83b4-109">예제 1: 컨테이너 서비스 만들기</span><span class="sxs-lookup"><span data-stu-id="f83b4-109">Example 1: Create a container service</span></span>
```
PS C:\> New-AzResourceGroup -Name "ResourceGroup17" -Location "East US" -Force
PS C:\> $Container = New-AzContainerServiceConfig -Location "East US" -OrchestratorType "DCOS" -MasterDnsPrefix "MasterResourceGroup17" -AdminUsername "acslinuxadmin" -SshPublicKey "<ssh-key>" | Add-AzContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17" -Count 2
PS C:\> New-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" -ContainerService $Container
```

<span data-ttu-id="f83b4-110">첫 번째 명령은 지정된 위치에 ResourceGroup17이라는 리소스 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f83b4-110">The first command creates a resource group named ResourceGroup17 at the specified location.</span></span>
<span data-ttu-id="f83b4-111">자세한 내용은 다음 cmdlet을 New-AzResourceGroup 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f83b4-111">For more information, see the New-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="f83b4-112">두 번째 명령은 컨테이너를 만든 다음 컨테이너를 $Container 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="f83b4-112">The second command creates a container, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="f83b4-113">자세한 내용은 다음 cmdlet을 New-AzContainerServiceConfig 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f83b4-113">For more information, see the New-AzContainerServiceConfig cmdlet.</span></span>
<span data-ttu-id="f83b4-114">마지막 명령은 컨테이너에 저장된 컨테이너에 대한 컨테이너 서비스를 $Container.</span><span class="sxs-lookup"><span data-stu-id="f83b4-114">The final command creates a container service for the container stored in $Container.</span></span>
<span data-ttu-id="f83b4-115">서비스 이름은 csResourceGroup17입니다.</span><span class="sxs-lookup"><span data-stu-id="f83b4-115">The service is named csResourceGroup17.</span></span>

## <span data-ttu-id="f83b4-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f83b4-116">PARAMETERS</span></span>

### <span data-ttu-id="f83b4-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f83b4-117">-AsJob</span></span>
<span data-ttu-id="f83b4-118">백그라운드에서 RRun cmdlet을 실행하고 진행률을 추적하는 작업을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="f83b4-118">RRun cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="f83b4-119">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="f83b4-119">-ContainerService</span></span>
<span data-ttu-id="f83b4-120">새 서비스에 대한 속성을 포함하는 컨테이너 서비스 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f83b4-120">Specifies a container service object that contains the properties for the new service.</span></span>
<span data-ttu-id="f83b4-121">**ContainerService** 개체를 얻으면 New-AzContainerServiceConfig cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="f83b4-121">To obtain a **ContainerService** object, use the New-AzContainerServiceConfig cmdlet.</span></span>

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

### <span data-ttu-id="f83b4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f83b4-122">-DefaultProfile</span></span>
<span data-ttu-id="f83b4-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f83b4-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f83b4-124">-Name</span><span class="sxs-lookup"><span data-stu-id="f83b4-124">-Name</span></span>
<span data-ttu-id="f83b4-125">이 cmdlet에서 만드는 컨테이너 서비스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f83b4-125">Specifies the name of the container service that this cmdlet creates.</span></span>

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

### <span data-ttu-id="f83b4-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f83b4-126">-ResourceGroupName</span></span>
<span data-ttu-id="f83b4-127">이 cmdlet이 컨테이너 서비스를 배포하는 리소스 그룹을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f83b4-127">Specifies the resource group in which this cmdlet deploys the container service.</span></span>

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

### <span data-ttu-id="f83b4-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f83b4-128">-Confirm</span></span>
<span data-ttu-id="f83b4-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f83b4-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f83b4-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f83b4-130">-WhatIf</span></span>
<span data-ttu-id="f83b4-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="f83b4-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f83b4-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f83b4-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f83b4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f83b4-133">CommonParameters</span></span>
<span data-ttu-id="f83b4-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f83b4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f83b4-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f83b4-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f83b4-136">입력</span><span class="sxs-lookup"><span data-stu-id="f83b4-136">INPUTS</span></span>

### <span data-ttu-id="f83b4-137">System.String</span><span class="sxs-lookup"><span data-stu-id="f83b4-137">System.String</span></span>

### <span data-ttu-id="f83b4-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span><span class="sxs-lookup"><span data-stu-id="f83b4-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="f83b4-139">출력</span><span class="sxs-lookup"><span data-stu-id="f83b4-139">OUTPUTS</span></span>

### <span data-ttu-id="f83b4-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span><span class="sxs-lookup"><span data-stu-id="f83b4-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="f83b4-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f83b4-141">NOTES</span></span>

## <span data-ttu-id="f83b4-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f83b4-142">RELATED LINKS</span></span>

[<span data-ttu-id="f83b4-143">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="f83b4-143">Get-AzContainerService</span></span>](./Get-AzContainerService.md)

[<span data-ttu-id="f83b4-144">New-AzContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="f83b4-144">New-AzContainerServiceConfig</span></span>](./New-AzContainerServiceConfig.md)

[<span data-ttu-id="f83b4-145">Remove-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="f83b4-145">Remove-AzContainerService</span></span>](./Remove-AzContainerService.md)

[<span data-ttu-id="f83b4-146">Update-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="f83b4-146">Update-AzContainerService</span></span>](./Update-AzContainerService.md)


