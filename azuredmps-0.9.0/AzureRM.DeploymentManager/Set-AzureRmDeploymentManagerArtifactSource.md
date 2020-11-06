---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/set-azurermdeploymentmanagerartifactsource
schema: 2.0.0
ms.openlocfilehash: 230e443fad4740b6bf9896164f02ae9b382e3ed2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523336"
---
# <span data-ttu-id="dacc7-101">Set-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="dacc7-101">Set-AzureRmDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="dacc7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dacc7-102">SYNOPSIS</span></span>
<span data-ttu-id="dacc7-103">아티팩트 원본을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="dacc7-103">Updates an artifact source.</span></span>

## <span data-ttu-id="dacc7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dacc7-104">SYNTAX</span></span>

```
Set-AzureRmDeploymentManagerArtifactSource [-ArtifactSource] <PSArtifactSource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dacc7-105">설명은</span><span class="sxs-lookup"><span data-stu-id="dacc7-105">DESCRIPTION</span></span>
<span data-ttu-id="dacc7-106">**AzureRmDeploymentManagerArtifactSource** cmdlet은 지정 된 아티팩트 원본 개체를 사용 하 여 아티팩트 원본을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="dacc7-106">The **Set-AzureRmDeploymentManagerArtifactSource** cmdlet updates an artifact source with the specified artifact source object.</span></span>
<span data-ttu-id="dacc7-107">Cmdlet은 업데이트 된 ArtifactSource 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="dacc7-107">The cmdlet returns the updated ArtifactSource object.</span></span>

## <span data-ttu-id="dacc7-108">예제의</span><span class="sxs-lookup"><span data-stu-id="dacc7-108">EXAMPLES</span></span>

### <span data-ttu-id="dacc7-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="dacc7-109">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerArtifactSource -ArtifactSource $artifactSourceObject
```

<span data-ttu-id="dacc7-110">이 명령은 name 및 ResourceGroup이 $artifactSourceObject의 Name 및 ResourceGroupName 속성과 각각 일치 하는 아티팩트 원본을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="dacc7-110">This command updates an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>
<span data-ttu-id="dacc7-111">아티팩트 소스가 $artifactSourceObject에 설정 된 속성으로 업데이트 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dacc7-111">The artifact source would be updated to the properties set in the $artifactSourceObject.</span></span>

## <span data-ttu-id="dacc7-112">변수</span><span class="sxs-lookup"><span data-stu-id="dacc7-112">PARAMETERS</span></span>

### <span data-ttu-id="dacc7-113">-ArtifactSource</span><span class="sxs-lookup"><span data-stu-id="dacc7-113">-ArtifactSource</span></span>
<span data-ttu-id="dacc7-114">아티팩트 원본 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="dacc7-114">The artifact source object.</span></span>

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

### <span data-ttu-id="dacc7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dacc7-115">-DefaultProfile</span></span>
<span data-ttu-id="dacc7-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dacc7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dacc7-117">-확인</span><span class="sxs-lookup"><span data-stu-id="dacc7-117">-Confirm</span></span>
<span data-ttu-id="dacc7-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="dacc7-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dacc7-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dacc7-119">-WhatIf</span></span>
<span data-ttu-id="dacc7-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="dacc7-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dacc7-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dacc7-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dacc7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dacc7-122">CommonParameters</span></span>
<span data-ttu-id="dacc7-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dacc7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dacc7-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dacc7-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dacc7-125">입력</span><span class="sxs-lookup"><span data-stu-id="dacc7-125">INPUTS</span></span>

### <span data-ttu-id="dacc7-126">Microsoft Azure.. i m a 관리자. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="dacc7-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="dacc7-127">출력</span><span class="sxs-lookup"><span data-stu-id="dacc7-127">OUTPUTS</span></span>

### <span data-ttu-id="dacc7-128">Microsoft Azure.. i m a 관리자. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="dacc7-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="dacc7-129">상속자</span><span class="sxs-lookup"><span data-stu-id="dacc7-129">NOTES</span></span>

## <span data-ttu-id="dacc7-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dacc7-130">RELATED LINKS</span></span>

[<span data-ttu-id="dacc7-131">새로운 AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="dacc7-131">New-AzureRmDeploymentManagerArtifactSource</span></span>](./New-AzureRmDeploymentManagerArtifactSource.md)

[<span data-ttu-id="dacc7-132">Get-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="dacc7-132">Get-AzureRmDeploymentManagerArtifactSource</span></span>](./Get-AzureRmDeploymentManagerArtifactSource.md)

[<span data-ttu-id="dacc7-133">제거-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="dacc7-133">Remove-AzureRmDeploymentManagerArtifactSource</span></span>](./Remove-AzureRmDeploymentManagerArtifactSource.md)