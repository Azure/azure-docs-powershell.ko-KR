---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/set-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: 9d5d79f65adbcab7ce61ad125e78189d0f84f9a7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980592"
---
# <span data-ttu-id="02e91-101">Set-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="02e91-101">Set-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="02e91-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02e91-102">SYNOPSIS</span></span>
<span data-ttu-id="02e91-103">아티팩트 원본을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="02e91-103">Updates the artifacts source.</span></span>

## <span data-ttu-id="02e91-104">구문</span><span class="sxs-lookup"><span data-stu-id="02e91-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerArtifactSource [-InputObject] <PSArtifactSource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02e91-105">설명</span><span class="sxs-lookup"><span data-stu-id="02e91-105">DESCRIPTION</span></span>
<span data-ttu-id="02e91-106">**Set-AzDeploymentManagerArtifactSource** cmdlet은 지정된 아티팩트 원본 개체로 아티팩트 원본을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="02e91-106">The **Set-AzDeploymentManagerArtifactSource** cmdlet updates an artifact source with the specified artifact source object.</span></span>
<span data-ttu-id="02e91-107">cmdlet은 업데이트된 ArtifactSource 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="02e91-107">The cmdlet returns the updated ArtifactSource object.</span></span>

## <span data-ttu-id="02e91-108">예제</span><span class="sxs-lookup"><span data-stu-id="02e91-108">EXAMPLES</span></span>

### <span data-ttu-id="02e91-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="02e91-109">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -InputObject $artifactSourceObject
```

<span data-ttu-id="02e91-110">이 명령은 이름 및 ResourceGroup이 각각 해당 리소스의 이름 및 ResourceGroupName 속성과 일치하는 아티팩트 $artifactSourceObject 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="02e91-110">This command updates an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>
<span data-ttu-id="02e91-111">아티팩트 원본은 해당 아티팩트에 설정된 속성으로 $artifactSourceObject.</span><span class="sxs-lookup"><span data-stu-id="02e91-111">The artifact source would be updated to the properties set in the $artifactSourceObject.</span></span>

## <span data-ttu-id="02e91-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="02e91-112">PARAMETERS</span></span>

### <span data-ttu-id="02e91-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02e91-113">-DefaultProfile</span></span>
<span data-ttu-id="02e91-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="02e91-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02e91-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="02e91-115">-InputObject</span></span>
<span data-ttu-id="02e91-116">아티팩트 원본 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="02e91-116">The artifact source object.</span></span>

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

### <span data-ttu-id="02e91-117">-확인</span><span class="sxs-lookup"><span data-stu-id="02e91-117">-Confirm</span></span>
<span data-ttu-id="02e91-118">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="02e91-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02e91-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02e91-119">-WhatIf</span></span>
<span data-ttu-id="02e91-120">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="02e91-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02e91-121">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="02e91-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02e91-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02e91-122">CommonParameters</span></span>
<span data-ttu-id="02e91-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="02e91-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02e91-124">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="02e91-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02e91-125">입력</span><span class="sxs-lookup"><span data-stu-id="02e91-125">INPUTS</span></span>

### <span data-ttu-id="02e91-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="02e91-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="02e91-127">출력</span><span class="sxs-lookup"><span data-stu-id="02e91-127">OUTPUTS</span></span>

### <span data-ttu-id="02e91-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="02e91-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="02e91-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="02e91-129">NOTES</span></span>

## <span data-ttu-id="02e91-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="02e91-130">RELATED LINKS</span></span>
