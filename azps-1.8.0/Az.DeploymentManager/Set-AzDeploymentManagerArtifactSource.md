---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: 32e5293f7c5bb62711a6510c590aa1ba7f4229b7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700975"
---
# <span data-ttu-id="ec9fb-101">Set-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="ec9fb-101">Set-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="ec9fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec9fb-102">SYNOPSIS</span></span>
<span data-ttu-id="ec9fb-103">아티팩트 원본을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec9fb-103">Updates the artifacts source.</span></span>

## <span data-ttu-id="ec9fb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ec9fb-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerArtifactSource [-InputObject] <PSArtifactSource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec9fb-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ec9fb-105">DESCRIPTION</span></span>
<span data-ttu-id="ec9fb-106">**AzDeploymentManagerArtifactSource** cmdlet은 지정 된 아티팩트 원본 개체를 사용 하 여 아티팩트 원본을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec9fb-106">The **Set-AzDeploymentManagerArtifactSource** cmdlet updates an artifact source with the specified artifact source object.</span></span>
<span data-ttu-id="ec9fb-107">Cmdlet은 업데이트 된 ArtifactSource 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec9fb-107">The cmdlet returns the updated ArtifactSource object.</span></span>

## <span data-ttu-id="ec9fb-108">예제의</span><span class="sxs-lookup"><span data-stu-id="ec9fb-108">EXAMPLES</span></span>

### <span data-ttu-id="ec9fb-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="ec9fb-109">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -InputObject $artifactSourceObject
```

<span data-ttu-id="ec9fb-110">이 명령은 name 및 ResourceGroup이 $artifactSourceObject의 Name 및 ResourceGroupName 속성과 각각 일치 하는 아티팩트 원본을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec9fb-110">This command updates an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>
<span data-ttu-id="ec9fb-111">아티팩트 소스가 $artifactSourceObject에 설정 된 속성으로 업데이트 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ec9fb-111">The artifact source would be updated to the properties set in the $artifactSourceObject.</span></span>

## <span data-ttu-id="ec9fb-112">변수</span><span class="sxs-lookup"><span data-stu-id="ec9fb-112">PARAMETERS</span></span>

### <span data-ttu-id="ec9fb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec9fb-113">-DefaultProfile</span></span>
<span data-ttu-id="ec9fb-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ec9fb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec9fb-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ec9fb-115">-InputObject</span></span>
<span data-ttu-id="ec9fb-116">아티팩트 원본 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="ec9fb-116">The artifact source object.</span></span>

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

### <span data-ttu-id="ec9fb-117">-확인</span><span class="sxs-lookup"><span data-stu-id="ec9fb-117">-Confirm</span></span>
<span data-ttu-id="ec9fb-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec9fb-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec9fb-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec9fb-119">-WhatIf</span></span>
<span data-ttu-id="ec9fb-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ec9fb-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec9fb-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ec9fb-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec9fb-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec9fb-122">CommonParameters</span></span>
<span data-ttu-id="ec9fb-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec9fb-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec9fb-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec9fb-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec9fb-125">입력</span><span class="sxs-lookup"><span data-stu-id="ec9fb-125">INPUTS</span></span>

### <span data-ttu-id="ec9fb-126">Microsoft Azure.. i m a 관리자. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="ec9fb-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="ec9fb-127">출력</span><span class="sxs-lookup"><span data-stu-id="ec9fb-127">OUTPUTS</span></span>

### <span data-ttu-id="ec9fb-128">Microsoft Azure.. i m a 관리자. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="ec9fb-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="ec9fb-129">상속자</span><span class="sxs-lookup"><span data-stu-id="ec9fb-129">NOTES</span></span>

## <span data-ttu-id="ec9fb-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ec9fb-130">RELATED LINKS</span></span>