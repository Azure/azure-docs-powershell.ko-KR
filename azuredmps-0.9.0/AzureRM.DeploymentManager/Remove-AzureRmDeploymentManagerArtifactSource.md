---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/remove-azurermdeploymentmanagerartifactsource
schema: 2.0.0
ms.openlocfilehash: 7473f125511995efb1f6273d3b8adb675a58d06d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523080"
---
# <span data-ttu-id="34721-101">Remove-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="34721-101">Remove-AzureRmDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="34721-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34721-102">SYNOPSIS</span></span>
<span data-ttu-id="34721-103">아티팩트 원본을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="34721-103">Deletes an artifact source.</span></span>

## <span data-ttu-id="34721-104">구문과</span><span class="sxs-lookup"><span data-stu-id="34721-104">SYNTAX</span></span>

### <span data-ttu-id="34721-105">대화형 (기본값)</span><span class="sxs-lookup"><span data-stu-id="34721-105">Interactive (Default)</span></span>
```
Remove-AzureRmDeploymentManagerArtifactSource [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34721-106">리소스</span><span class="sxs-lookup"><span data-stu-id="34721-106">ResourceId</span></span>
```
Remove-AzureRmDeploymentManagerArtifactSource [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34721-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="34721-107">InputObject</span></span>
```
Remove-AzureRmDeploymentManagerArtifactSource [-ArtifactSource] <PSArtifactSource> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34721-108">설명은</span><span class="sxs-lookup"><span data-stu-id="34721-108">DESCRIPTION</span></span>
<span data-ttu-id="34721-109">**AzureRmDeploymentManagerArtifactSource** cmdlet은 아티팩트 원본을 삭제 하 고 해당 이름 및 리소스 그룹 이름을 기준으로 아티팩트 원본을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="34721-109">The **Remove-AzureRmDeploymentManagerArtifactSource** cmdlet deletes an artifact source Specify the artifact source by its name and resource group name.</span></span> <span data-ttu-id="34721-110">또는 ArtifactSource 개체 또는 ResourceId를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="34721-110">Alternately, you can provide the ArtifactSource object or the ResourceId.</span></span>

## <span data-ttu-id="34721-111">예제의</span><span class="sxs-lookup"><span data-stu-id="34721-111">EXAMPLES</span></span>

### <span data-ttu-id="34721-112">예제 1: 아티팩트 원본 삭제</span><span class="sxs-lookup"><span data-stu-id="34721-112">Example 1: Delete an artifact source</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerArtifactSource -ResourceGroupName "ContosoResourceGroup" -Name "ContosoArtifactSource"
```

<span data-ttu-id="34721-113">이 명령은 ContosoResourceGroup에서 ContosoArtifactSource 이라는 아티팩트 원본을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="34721-113">This command deletes an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="34721-114">예제 2: 리소스 식별자를 사용 하 여 아티팩트 원본 삭제</span><span class="sxs-lookup"><span data-stu-id="34721-114">Example 2: Delete an artifact source using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerArtifactSource -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="34721-115">이 명령은 ContosoResourceGroup에서 ContosoArtifactSource 이라는 아티팩트 원본을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="34721-115">This command deletes an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="34721-116">예제 3: 개체를 사용 하 여 아티팩트 원본 삭제</span><span class="sxs-lookup"><span data-stu-id="34721-116">Example 3: Delete an artifact source using an object</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerArtifactSource -ArtifactSource $artifactSourceObject
```

<span data-ttu-id="34721-117">이 명령은 name 및 ResourceGroup이 $artifactSourceObject의 Name 및 ResourceGroupName 속성과 각각 일치 하는 아티팩트 원본을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="34721-117">This command deletes an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>

## <span data-ttu-id="34721-118">변수</span><span class="sxs-lookup"><span data-stu-id="34721-118">PARAMETERS</span></span>

### <span data-ttu-id="34721-119">-ArtifactSource</span><span class="sxs-lookup"><span data-stu-id="34721-119">-ArtifactSource</span></span>
<span data-ttu-id="34721-120">제거할 아티팩트 저장소입니다.</span><span class="sxs-lookup"><span data-stu-id="34721-120">The artifact store to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="34721-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34721-121">-DefaultProfile</span></span>
<span data-ttu-id="34721-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="34721-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34721-123">-Force</span><span class="sxs-lookup"><span data-stu-id="34721-123">-Force</span></span>
<span data-ttu-id="34721-124">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="34721-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="34721-125">-이름</span><span class="sxs-lookup"><span data-stu-id="34721-125">-Name</span></span>
<span data-ttu-id="34721-126">아티팩트 원본의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="34721-126">The name of the artifact source.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34721-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="34721-127">-PassThru</span></span>
<span data-ttu-id="34721-128">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="34721-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="34721-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34721-129">-ResourceGroupName</span></span>
<span data-ttu-id="34721-130">리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="34721-130">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34721-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="34721-131">-ResourceId</span></span>
<span data-ttu-id="34721-132">리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="34721-132">The resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34721-133">-확인</span><span class="sxs-lookup"><span data-stu-id="34721-133">-Confirm</span></span>
<span data-ttu-id="34721-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="34721-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34721-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34721-135">-WhatIf</span></span>
<span data-ttu-id="34721-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="34721-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34721-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="34721-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34721-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34721-138">CommonParameters</span></span>
<span data-ttu-id="34721-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="34721-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34721-140">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34721-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34721-141">입력</span><span class="sxs-lookup"><span data-stu-id="34721-141">INPUTS</span></span>

### <span data-ttu-id="34721-142">Microsoft Azure.. i m a 관리자. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="34721-142">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="34721-143">출력</span><span class="sxs-lookup"><span data-stu-id="34721-143">OUTPUTS</span></span>

### <span data-ttu-id="34721-144">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="34721-144">System.Boolean</span></span>

## <span data-ttu-id="34721-145">상속자</span><span class="sxs-lookup"><span data-stu-id="34721-145">NOTES</span></span>

## <span data-ttu-id="34721-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="34721-146">RELATED LINKS</span></span>

[<span data-ttu-id="34721-147">새로운 AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="34721-147">New-AzureRmDeploymentManagerArtifactSource</span></span>](./New-AzureRmDeploymentManagerArtifactSource.md)

[<span data-ttu-id="34721-148">Get-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="34721-148">Get-AzureRmDeploymentManagerArtifactSource</span></span>](./Get-AzureRmDeploymentManagerArtifactSource.md)

[<span data-ttu-id="34721-149">Set-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="34721-149">Set-AzureRmDeploymentManagerArtifactSource</span></span>](./Set-AzureRmDeploymentManagerArtifactSource.md)