---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Get-AzDataMigrationProject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationProject.md
ms.openlocfilehash: 7fe1e12c7c7feb2a47ac33b309b188e53e77fc73
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327704"
---
# <span data-ttu-id="3dae4-101">Get-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="3dae4-101">Get-AzDataMigrationProject</span></span>

## <span data-ttu-id="3dae4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3dae4-102">SYNOPSIS</span></span>
<span data-ttu-id="3dae4-103">Azure Database Migration 프로젝트의 속성을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="3dae4-103">Retrieves the properties of an Azure Database Migration project.</span></span>

## <span data-ttu-id="3dae4-104">구문</span><span class="sxs-lookup"><span data-stu-id="3dae4-104">SYNTAX</span></span>

### <span data-ttu-id="3dae4-105">ComponentNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="3dae4-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzDataMigrationProject -ResourceGroupName <String> -ServiceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3dae4-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3dae4-106">ComponentObjectParameterSet</span></span>
```
Get-AzDataMigrationProject [-InputObject] <PSDataMigrationService> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3dae4-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3dae4-107">ResourceIdParameterSet</span></span>
```
Get-AzDataMigrationProject [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3dae4-108">설명</span><span class="sxs-lookup"><span data-stu-id="3dae4-108">DESCRIPTION</span></span>
<span data-ttu-id="3dae4-109">Get-AzDataMigrationProject cmdlet은 Azure Database Migration 프로젝트의 속성을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="3dae4-109">The Get-AzDataMigrationProject cmdlet retrieves the properties of an Azure Database Migration project.</span></span>

## <span data-ttu-id="3dae4-110">예제</span><span class="sxs-lookup"><span data-stu-id="3dae4-110">EXAMPLES</span></span>

### <span data-ttu-id="3dae4-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="3dae4-111">Example 1</span></span>
```
PS C:\> Get-AzDataMigrationProject -ServiceName testService -Name testProject -ResourceGroup testResourceGroup
```

<span data-ttu-id="3dae4-112">위의 예제에서는 testResourceGroup이라는 리소스 그룹 및 testService라는 서비스에서 TestProject라는 Azure Database Migration 프로젝트를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="3dae4-112">The above example retrieves  Azure Database Migration project named TestProject in the resource group called testResourceGroup and under service called testService</span></span>

### <span data-ttu-id="3dae4-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="3dae4-113">Example 2</span></span>
```
PS C:\> Get-AzDataMigrationProject -InputObject $myService
```

<span data-ttu-id="3dae4-114">위의 예제에서는 전달된 PSProject 개체 입력 매개 변수를 기반으로 Azure Database Migration 프로젝트를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="3dae4-114">The above example retrieves the  Azure Database Migration project based on PSProject object input parameter passed in.</span></span> 

## <span data-ttu-id="3dae4-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3dae4-115">PARAMETERS</span></span>

### <span data-ttu-id="3dae4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dae4-116">-DefaultProfile</span></span>
<span data-ttu-id="3dae4-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3dae4-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3dae4-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3dae4-118">-InputObject</span></span>
<span data-ttu-id="3dae4-119">PSDataMigrationService 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="3dae4-119">PSDataMigrationService Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService
Parameter Sets: ComponentObjectParameterSet
Aliases: DataMigrationService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3dae4-120">-Name</span><span class="sxs-lookup"><span data-stu-id="3dae4-120">-Name</span></span>
<span data-ttu-id="3dae4-121">프로젝트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3dae4-121">The name of the project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ProjectName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dae4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3dae4-122">-ResourceGroupName</span></span>
<span data-ttu-id="3dae4-123">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3dae4-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dae4-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3dae4-124">-ResourceId</span></span>
<span data-ttu-id="3dae4-125">DataMigrationService 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="3dae4-125">DataMigrationService Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dae4-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="3dae4-126">-ServiceName</span></span>
<span data-ttu-id="3dae4-127">Database Migration Service 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3dae4-127">Database Migration Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dae4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dae4-128">CommonParameters</span></span>
<span data-ttu-id="3dae4-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3dae4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dae4-130">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="3dae4-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dae4-131">입력</span><span class="sxs-lookup"><span data-stu-id="3dae4-131">INPUTS</span></span>

### <span data-ttu-id="3dae4-132">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="3dae4-132">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="3dae4-133">System.String</span><span class="sxs-lookup"><span data-stu-id="3dae4-133">System.String</span></span>

## <span data-ttu-id="3dae4-134">출력</span><span class="sxs-lookup"><span data-stu-id="3dae4-134">OUTPUTS</span></span>

### <span data-ttu-id="3dae4-135">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span><span class="sxs-lookup"><span data-stu-id="3dae4-135">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

## <span data-ttu-id="3dae4-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3dae4-136">NOTES</span></span>

## <span data-ttu-id="3dae4-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3dae4-137">RELATED LINKS</span></span>
