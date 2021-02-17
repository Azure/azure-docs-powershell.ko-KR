---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: ee69c178d48775a870b229e652a1584c413bd7ca
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208605"
---
# <span data-ttu-id="62fd5-101">Set-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="62fd5-101">Set-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="62fd5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62fd5-102">SYNOPSIS</span></span>
<span data-ttu-id="62fd5-103">아티팩트 원본을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="62fd5-103">Updates the artifacts source.</span></span>

## <span data-ttu-id="62fd5-104">구문</span><span class="sxs-lookup"><span data-stu-id="62fd5-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerArtifactSource [-InputObject] <PSArtifactSource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62fd5-105">설명</span><span class="sxs-lookup"><span data-stu-id="62fd5-105">DESCRIPTION</span></span>
<span data-ttu-id="62fd5-106">**Set-AzDeploymentManagerArtifactSource** cmdlet은 지정된 아티팩트 원본 개체를 통해 아티팩트 원본을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="62fd5-106">The **Set-AzDeploymentManagerArtifactSource** cmdlet updates an artifact source with the specified artifact source object.</span></span>
<span data-ttu-id="62fd5-107">cmdlet은 업데이트된 ArtifactSource 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="62fd5-107">The cmdlet returns the updated ArtifactSource object.</span></span>

## <span data-ttu-id="62fd5-108">예제</span><span class="sxs-lookup"><span data-stu-id="62fd5-108">EXAMPLES</span></span>

### <span data-ttu-id="62fd5-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="62fd5-109">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -InputObject $artifactSourceObject
```

<span data-ttu-id="62fd5-110">이 명령은 이름과 ResourceGroup이 각각 이름 및 ResourceGroupName 속성과 일치하는 아티팩트 $artifactSourceObject 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="62fd5-110">This command updates an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>
<span data-ttu-id="62fd5-111">아티팩트 원본은 아티팩트 원본에 설정된 속성으로 $artifactSourceObject.</span><span class="sxs-lookup"><span data-stu-id="62fd5-111">The artifact source would be updated to the properties set in the $artifactSourceObject.</span></span>

## <span data-ttu-id="62fd5-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="62fd5-112">PARAMETERS</span></span>

### <span data-ttu-id="62fd5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62fd5-113">-DefaultProfile</span></span>
<span data-ttu-id="62fd5-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="62fd5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62fd5-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="62fd5-115">-InputObject</span></span>
<span data-ttu-id="62fd5-116">아티팩트 원본 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="62fd5-116">The artifact source object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="62fd5-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="62fd5-117">-Confirm</span></span>
<span data-ttu-id="62fd5-118">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="62fd5-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62fd5-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62fd5-119">-WhatIf</span></span>
<span data-ttu-id="62fd5-120">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="62fd5-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62fd5-121">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="62fd5-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62fd5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62fd5-122">CommonParameters</span></span>
<span data-ttu-id="62fd5-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="62fd5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62fd5-124">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="62fd5-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62fd5-125">입력</span><span class="sxs-lookup"><span data-stu-id="62fd5-125">INPUTS</span></span>

### <span data-ttu-id="62fd5-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="62fd5-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="62fd5-127">출력</span><span class="sxs-lookup"><span data-stu-id="62fd5-127">OUTPUTS</span></span>

### <span data-ttu-id="62fd5-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="62fd5-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="62fd5-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="62fd5-129">NOTES</span></span>

## <span data-ttu-id="62fd5-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="62fd5-130">RELATED LINKS</span></span>
