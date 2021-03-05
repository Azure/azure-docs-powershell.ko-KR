---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/new-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: 8aab061d7f61605273bd7147dc5a85ca45bf8ad0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966320"
---
# <span data-ttu-id="4dce2-101">New-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="4dce2-101">New-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="4dce2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4dce2-102">SYNOPSIS</span></span>
<span data-ttu-id="4dce2-103">아티팩트 원본을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4dce2-103">Creates an artifact source.</span></span>

## <span data-ttu-id="4dce2-104">구문</span><span class="sxs-lookup"><span data-stu-id="4dce2-104">SYNTAX</span></span>

```
New-AzDeploymentManagerArtifactSource -ResourceGroupName <String> -Name <String> -Location <String>
 -SasUri <String> [-Tag <Hashtable>] [-ArtifactRoot <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4dce2-105">설명</span><span class="sxs-lookup"><span data-stu-id="4dce2-105">DESCRIPTION</span></span>
<span data-ttu-id="4dce2-106">**New-AzDeploymentManagerArtifactSource** cmdlet은 아티팩트 원본을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4dce2-106">The **New-AzDeploymentManagerArtifactSource** cmdlet creates an artifact source.</span></span>
<span data-ttu-id="4dce2-107">*이름,* *ResourceGroupName 및* 필수 속성을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4dce2-107">Specify the *Name*, *ResourceGroupName* and required properties.</span></span>

<span data-ttu-id="4dce2-108">반환된 개체를 로컬로 수정한 다음, cmdlet을 사용하여 아티팩트 원본에 Set-AzDeploymentManagerArtifactSource 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4dce2-108">You can modify the returned object locally and then apply the changes to the artifact source by using the Set-AzDeploymentManagerArtifactSource cmdlet.</span></span>

<span data-ttu-id="4dce2-109">cmdlet은 ServiceUnit 리소스, 템플릿 및 매개 변수 파일에 필요한 아티팩트를 이 위치에서 참조할 수 있도록 New-AzDeploymentManagerServiceTopology cmdlet에서 참조할 수 있는 ResourceId가 있는 ArtifactSource 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="4dce2-109">The cmdlet returns an ArtifactSource object that has a ResourceId which can be referenced in the New-AzDeploymentManagerServiceTopology cmdlet so that artifacts required for a ServiceUnit resource, the Template and Parameters files, can be referenced from this location.</span></span>

## <span data-ttu-id="4dce2-110">예제</span><span class="sxs-lookup"><span data-stu-id="4dce2-110">EXAMPLES</span></span>

### <span data-ttu-id="4dce2-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="4dce2-111">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerArtifactSource -ResourceGroupName ContosoResourceGroup -Name ContosoArtifactSource -Location "Central US" -SasUri "https://ContosoStorage.blob.core.windows.net/ContosoArtifacts?sasParameters"
```

<span data-ttu-id="4dce2-112">ContosoResourceGroup에서 리소스의 위치로 미국 중부와 함께 ContosoArtifactSource 이름이 있는 아티팩트 원본을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4dce2-112">Creates an artifact source in the ContosoResourceGroup with the name ContosoArtifactSource with Central US as the location of the resource.</span></span> <span data-ttu-id="4dce2-113">SasUri 속성은 아티팩트가 저장되는 저장소 컨테이너에 Azure Storage SAS Uri를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="4dce2-113">The SasUri property provides an Azure Storage SAS Uri to the storage container where the artifacts are stored.</span></span>

## <span data-ttu-id="4dce2-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="4dce2-114">PARAMETERS</span></span>

### <span data-ttu-id="4dce2-115">-ArtifactRoot</span><span class="sxs-lookup"><span data-stu-id="4dce2-115">-ArtifactRoot</span></span>
<span data-ttu-id="4dce2-116">아티팩트의 저장소 컨테이너 아래에 있는 선택적 디렉터리 오프셋입니다.</span><span class="sxs-lookup"><span data-stu-id="4dce2-116">The optional directory offset under the storage container for the artifacts.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dce2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dce2-117">-DefaultProfile</span></span>
<span data-ttu-id="4dce2-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4dce2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4dce2-119">-Location</span><span class="sxs-lookup"><span data-stu-id="4dce2-119">-Location</span></span>
<span data-ttu-id="4dce2-120">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="4dce2-120">The location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dce2-121">-Name</span><span class="sxs-lookup"><span data-stu-id="4dce2-121">-Name</span></span>
<span data-ttu-id="4dce2-122">아티팩트 원본의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4dce2-122">The name of the artifact source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dce2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4dce2-123">-ResourceGroupName</span></span>
<span data-ttu-id="4dce2-124">리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="4dce2-124">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dce2-125">-SasUri</span><span class="sxs-lookup"><span data-stu-id="4dce2-125">-SasUri</span></span>
<span data-ttu-id="4dce2-126">아티팩트가 저장되는 Azure Storage 컨테이너에 대한 SAS Uri입니다.</span><span class="sxs-lookup"><span data-stu-id="4dce2-126">The SAS Uri to the Azure storage container where the artifacts are stored.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dce2-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="4dce2-127">-Tag</span></span>
<span data-ttu-id="4dce2-128">리소스 태그를 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="4dce2-128">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dce2-129">-확인</span><span class="sxs-lookup"><span data-stu-id="4dce2-129">-Confirm</span></span>
<span data-ttu-id="4dce2-130">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4dce2-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4dce2-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4dce2-131">-WhatIf</span></span>
<span data-ttu-id="4dce2-132">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="4dce2-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4dce2-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4dce2-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4dce2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dce2-134">CommonParameters</span></span>
<span data-ttu-id="4dce2-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4dce2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dce2-136">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4dce2-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dce2-137">입력</span><span class="sxs-lookup"><span data-stu-id="4dce2-137">INPUTS</span></span>

### <span data-ttu-id="4dce2-138">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="4dce2-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="4dce2-139">출력</span><span class="sxs-lookup"><span data-stu-id="4dce2-139">OUTPUTS</span></span>

### <span data-ttu-id="4dce2-140">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="4dce2-140">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="4dce2-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4dce2-141">NOTES</span></span>

## <span data-ttu-id="4dce2-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4dce2-142">RELATED LINKS</span></span>
