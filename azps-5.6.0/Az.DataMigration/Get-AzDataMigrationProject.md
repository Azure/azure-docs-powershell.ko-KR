---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/Get-AzDataMigrationProject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationProject.md
ms.openlocfilehash: 5485693da87dbbb49b5e06e221e818de9bd222d9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995568"
---
# <span data-ttu-id="094a3-101">Get-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="094a3-101">Get-AzDataMigrationProject</span></span>

## <span data-ttu-id="094a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="094a3-102">SYNOPSIS</span></span>
<span data-ttu-id="094a3-103">Azure Database Migration 프로젝트의 속성을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="094a3-103">Retrieves the properties of an Azure Database Migration project.</span></span>

## <span data-ttu-id="094a3-104">구문</span><span class="sxs-lookup"><span data-stu-id="094a3-104">SYNTAX</span></span>

### <span data-ttu-id="094a3-105">ComponentNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="094a3-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzDataMigrationProject -ResourceGroupName <String> -ServiceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="094a3-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="094a3-106">ComponentObjectParameterSet</span></span>
```
Get-AzDataMigrationProject [-InputObject] <PSDataMigrationService> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="094a3-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="094a3-107">ResourceIdParameterSet</span></span>
```
Get-AzDataMigrationProject [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="094a3-108">설명</span><span class="sxs-lookup"><span data-stu-id="094a3-108">DESCRIPTION</span></span>
<span data-ttu-id="094a3-109">Get-AzDataMigrationProject cmdlet은 Azure Database Migration 프로젝트의 속성을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="094a3-109">The Get-AzDataMigrationProject cmdlet retrieves the properties of an Azure Database Migration project.</span></span>

## <span data-ttu-id="094a3-110">예제</span><span class="sxs-lookup"><span data-stu-id="094a3-110">EXAMPLES</span></span>

### <span data-ttu-id="094a3-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="094a3-111">Example 1</span></span>
```
PS C:\> Get-AzDataMigrationProject -ServiceName testService -Name testProject -ResourceGroup testResourceGroup
```

<span data-ttu-id="094a3-112">위의 예제에서는 testResourceGroup이라는 리소스 그룹과 testService라는 서비스에서 TestProject라는 Azure Database Migration 프로젝트를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="094a3-112">The above example retrieves  Azure Database Migration project named TestProject in the resource group called testResourceGroup and under service called testService</span></span>

### <span data-ttu-id="094a3-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="094a3-113">Example 2</span></span>
```
PS C:\> Get-AzDataMigrationProject -InputObject $myService
```

<span data-ttu-id="094a3-114">위의 예제에서는 전달된 PSProject 개체 입력 매개 변수를 기반으로 Azure Database Migration 프로젝트를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="094a3-114">The above example retrieves the  Azure Database Migration project based on PSProject object input parameter passed in.</span></span> 

## <span data-ttu-id="094a3-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="094a3-115">PARAMETERS</span></span>

### <span data-ttu-id="094a3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="094a3-116">-DefaultProfile</span></span>
<span data-ttu-id="094a3-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="094a3-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="094a3-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="094a3-118">-InputObject</span></span>
<span data-ttu-id="094a3-119">PSDataMigrationService 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="094a3-119">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="094a3-120">-Name</span><span class="sxs-lookup"><span data-stu-id="094a3-120">-Name</span></span>
<span data-ttu-id="094a3-121">프로젝트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="094a3-121">The name of the project.</span></span>

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

### <span data-ttu-id="094a3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="094a3-122">-ResourceGroupName</span></span>
<span data-ttu-id="094a3-123">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="094a3-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="094a3-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="094a3-124">-ResourceId</span></span>
<span data-ttu-id="094a3-125">DataMigrationService 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="094a3-125">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="094a3-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="094a3-126">-ServiceName</span></span>
<span data-ttu-id="094a3-127">데이터베이스 마이그레이션 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="094a3-127">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="094a3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="094a3-128">CommonParameters</span></span>
<span data-ttu-id="094a3-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="094a3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="094a3-130">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="094a3-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="094a3-131">입력</span><span class="sxs-lookup"><span data-stu-id="094a3-131">INPUTS</span></span>

### <span data-ttu-id="094a3-132">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="094a3-132">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="094a3-133">System.String</span><span class="sxs-lookup"><span data-stu-id="094a3-133">System.String</span></span>

## <span data-ttu-id="094a3-134">출력</span><span class="sxs-lookup"><span data-stu-id="094a3-134">OUTPUTS</span></span>

### <span data-ttu-id="094a3-135">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span><span class="sxs-lookup"><span data-stu-id="094a3-135">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

## <span data-ttu-id="094a3-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="094a3-136">NOTES</span></span>

## <span data-ttu-id="094a3-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="094a3-137">RELATED LINKS</span></span>
