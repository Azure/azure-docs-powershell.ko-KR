---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: 09feb94b046ef6a41130c26ae5e7b996ecbd8771
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701000"
---
# <span data-ttu-id="7c1df-101">New-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="7c1df-101">New-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="7c1df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c1df-102">SYNOPSIS</span></span>
<span data-ttu-id="7c1df-103">아티팩트 원본을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7c1df-103">Creates an artifact source.</span></span>

## <span data-ttu-id="7c1df-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7c1df-104">SYNTAX</span></span>

```
New-AzDeploymentManagerArtifactSource -ResourceGroupName <String> -Name <String> -Location <String>
 -SasUri <String> [-Tag <Hashtable>] [-ArtifactRoot <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c1df-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7c1df-105">DESCRIPTION</span></span>
<span data-ttu-id="7c1df-106">**AzDeploymentManagerArtifactSource** cmdlet은 아티팩트 원본을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7c1df-106">The **New-AzDeploymentManagerArtifactSource** cmdlet creates an artifact source.</span></span>
<span data-ttu-id="7c1df-107">*Name* , *ResourceGroupName* 및 required 속성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c1df-107">Specify the *Name* , *ResourceGroupName* and required properties.</span></span>

<span data-ttu-id="7c1df-108">반환 된 개체를 로컬로 수정한 다음 Set-AzDeploymentManagerArtifactSource cmdlet을 사용 하 여 아티팩트 원본에 변경 내용을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7c1df-108">You can modify the returned object locally and then apply the changes to the artifact source by using the Set-AzDeploymentManagerArtifactSource cmdlet.</span></span>

<span data-ttu-id="7c1df-109">Cmdlet은 ServiceUnit 리소스, 템플릿 및 매개 변수 파일에 필요한 아티팩트를이 위치에서 참조할 수 있도록 New-AzDeloymentManagerServiceTopology cmdlet에서 참조할 수 있는 ResourceId가 있는 ArtifactSource 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c1df-109">The cmdlet returns an ArtifactSource object that has a ResourceId which can be referenced in the New-AzDeloymentManagerServiceTopology cmdlet so that artifacts required for a ServiceUnit resource, the Template and Parameters files, can be referenced from this location.</span></span>

## <span data-ttu-id="7c1df-110">예제의</span><span class="sxs-lookup"><span data-stu-id="7c1df-110">EXAMPLES</span></span>

### <span data-ttu-id="7c1df-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="7c1df-111">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerArtifactSource -ResourceGroupName ContosoResourceGroup -Name ContosoArtifactSource -Location "Central US" -SasUri "https://ContosoStorage.blob.core.windows.net/ContosoArtifacts?sasParameters"
```

<span data-ttu-id="7c1df-112">중앙 US와 이름이 ContosoArtifactSource 인 ContosoResourceGroup에서 리소스 위치로 아티팩트 원본을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7c1df-112">Creates an artifact source in the ContosoResourceGroup with the name ContosoArtifactSource with Central US as the location of the resource.</span></span> <span data-ttu-id="7c1df-113">SasUri 속성은 아티팩트가 저장 된 저장소 컨테이너에 대 한 Azure 저장소 SAS Uri를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c1df-113">The SasUri property provides an Azure Storage SAS Uri to the storage container where the artifacts are stored.</span></span>

## <span data-ttu-id="7c1df-114">변수</span><span class="sxs-lookup"><span data-stu-id="7c1df-114">PARAMETERS</span></span>

### <span data-ttu-id="7c1df-115">-ArtifactRoot</span><span class="sxs-lookup"><span data-stu-id="7c1df-115">-ArtifactRoot</span></span>
<span data-ttu-id="7c1df-116">아티팩트의 저장소 컨테이너 아래에 있는 선택적 디렉터리 오프셋입니다.</span><span class="sxs-lookup"><span data-stu-id="7c1df-116">The optional directory offset under the storage container for the artifacts.</span></span>

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

### <span data-ttu-id="7c1df-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c1df-117">-DefaultProfile</span></span>
<span data-ttu-id="7c1df-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7c1df-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c1df-119">-위치</span><span class="sxs-lookup"><span data-stu-id="7c1df-119">-Location</span></span>
<span data-ttu-id="7c1df-120">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="7c1df-120">The location of the resource.</span></span>

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

### <span data-ttu-id="7c1df-121">-이름</span><span class="sxs-lookup"><span data-stu-id="7c1df-121">-Name</span></span>
<span data-ttu-id="7c1df-122">아티팩트 원본의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7c1df-122">The name of the artifact source.</span></span>

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

### <span data-ttu-id="7c1df-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c1df-123">-ResourceGroupName</span></span>
<span data-ttu-id="7c1df-124">리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="7c1df-124">The resource group.</span></span>

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

### <span data-ttu-id="7c1df-125">-SasUri</span><span class="sxs-lookup"><span data-stu-id="7c1df-125">-SasUri</span></span>
<span data-ttu-id="7c1df-126">아티팩트가 저장 된 Azure storage 컨테이너에 대 한 SAS Uri입니다.</span><span class="sxs-lookup"><span data-stu-id="7c1df-126">The SAS Uri to the Azure storage container where the artifacts are stored.</span></span>

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

### <span data-ttu-id="7c1df-127">태그</span><span class="sxs-lookup"><span data-stu-id="7c1df-127">-Tag</span></span>
<span data-ttu-id="7c1df-128">리소스 태그를 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="7c1df-128">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="7c1df-129">-확인</span><span class="sxs-lookup"><span data-stu-id="7c1df-129">-Confirm</span></span>
<span data-ttu-id="7c1df-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c1df-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c1df-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c1df-131">-WhatIf</span></span>
<span data-ttu-id="7c1df-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7c1df-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c1df-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7c1df-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c1df-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c1df-134">CommonParameters</span></span>
<span data-ttu-id="7c1df-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c1df-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c1df-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c1df-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c1df-137">입력</span><span class="sxs-lookup"><span data-stu-id="7c1df-137">INPUTS</span></span>

### <span data-ttu-id="7c1df-138">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="7c1df-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="7c1df-139">출력</span><span class="sxs-lookup"><span data-stu-id="7c1df-139">OUTPUTS</span></span>

### <span data-ttu-id="7c1df-140">Microsoft Azure.. i m a 관리자. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="7c1df-140">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="7c1df-141">상속자</span><span class="sxs-lookup"><span data-stu-id="7c1df-141">NOTES</span></span>

## <span data-ttu-id="7c1df-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7c1df-142">RELATED LINKS</span></span>