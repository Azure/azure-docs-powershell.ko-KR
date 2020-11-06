---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/get-azurermdatamigrationproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationProject.md
ms.openlocfilehash: ea6406d83004d9a7d21a2f47aba0c39a10caf59a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534843"
---
# <span data-ttu-id="3f489-101">Get-AzureRmDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="3f489-101">Get-AzureRmDataMigrationProject</span></span>

## <span data-ttu-id="3f489-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f489-102">SYNOPSIS</span></span>
<span data-ttu-id="3f489-103">Azure 데이터베이스 마이그레이션 프로젝트의 속성을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f489-103">Retrieves the properties of an Azure Database Migration project.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f489-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3f489-104">SYNTAX</span></span>

### <span data-ttu-id="3f489-105">ComponentNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="3f489-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzureRmDataMigrationProject -ResourceGroupName <String> -ServiceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="3f489-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f489-106">ComponentObjectParameterSet</span></span>
```
Get-AzureRmDataMigrationProject [-InputObject] <PSDataMigrationService> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="3f489-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f489-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmDataMigrationProject [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="3f489-108">설명은</span><span class="sxs-lookup"><span data-stu-id="3f489-108">DESCRIPTION</span></span>
<span data-ttu-id="3f489-109">Get-AzureRmDataMigrationProject cmdlet은 Azure 데이터베이스 마이그레이션 프로젝트의 속성을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f489-109">The Get-AzureRmDataMigrationProject cmdlet retrieves the properties of an Azure Database Migration project.</span></span>

## <span data-ttu-id="3f489-110">예제의</span><span class="sxs-lookup"><span data-stu-id="3f489-110">EXAMPLES</span></span>

### <span data-ttu-id="3f489-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="3f489-111">Example 1</span></span>
```
PS C:\> Get-AzureRmDataMigrationProject -ServiceName testService -Name testProject -ResourceGroup testResourceGroup
```

<span data-ttu-id="3f489-112">위 예제에서는 리소스 그룹에서 testResourceGroup 이라는 TestProject 이라는 Azure 데이터베이스 마이그레이션 프로젝트를 검색 하 고 서비스에서 Testresourcegroup 라는 서비스로</span><span class="sxs-lookup"><span data-stu-id="3f489-112">The above example retrieves  Azure Database Migration project named TestProject in the resource group called testResourceGroup and under service called testService</span></span>

### <span data-ttu-id="3f489-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="3f489-113">Example 2</span></span>
```
PS C:\> Get-AzureRmDataMigrationProject -InputObject $myService
```

<span data-ttu-id="3f489-114">위 예제에서는 전달 된 PSProject 개체 입력 매개 변수를 기반으로 Azure 데이터베이스 마이그레이션 프로젝트를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f489-114">The above example retrieves the  Azure Database Migration project based on PSProject object input parameter passed in.</span></span> 


## <span data-ttu-id="3f489-115">변수</span><span class="sxs-lookup"><span data-stu-id="3f489-115">PARAMETERS</span></span>

### <span data-ttu-id="3f489-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f489-116">-DefaultProfile</span></span>
<span data-ttu-id="3f489-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3f489-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f489-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3f489-118">-InputObject</span></span>
<span data-ttu-id="3f489-119">PSDataMigrationService 개체</span><span class="sxs-lookup"><span data-stu-id="3f489-119">PSDataMigrationService Object.</span></span>

```yaml
Type: PSDataMigrationService
Parameter Sets: ComponentObjectParameterSet
Aliases: DataMigrationService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3f489-120">-이름</span><span class="sxs-lookup"><span data-stu-id="3f489-120">-Name</span></span>
<span data-ttu-id="3f489-121">프로젝트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3f489-121">The name of the project.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ProjectName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f489-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f489-122">-ResourceGroupName</span></span>
<span data-ttu-id="3f489-123">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3f489-123">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f489-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3f489-124">-ResourceId</span></span>
<span data-ttu-id="3f489-125">DataMigrationService 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="3f489-125">DataMigrationService Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f489-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="3f489-126">-ServiceName</span></span>
<span data-ttu-id="3f489-127">데이터 마이그레이션 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3f489-127">Data Migration Service Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="3f489-128">입력</span><span class="sxs-lookup"><span data-stu-id="3f489-128">INPUTS</span></span>

### <span data-ttu-id="3f489-129">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="3f489-129">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>
<span data-ttu-id="3f489-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="3f489-130">System.String</span></span>


## <span data-ttu-id="3f489-131">출력</span><span class="sxs-lookup"><span data-stu-id="3f489-131">OUTPUTS</span></span>

### <span data-ttu-id="3f489-132">System.webserver. IList ' 1 [[DataMigration 프로젝트, Microsoft Azure. DataMigration, Version = 0.1.0.0, Culture = 중립, PublicKeyToken = null]]을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f489-132">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.DataMigration.Models.PSProject, Microsoft.Azure.Commands.DataMigration, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>


## <span data-ttu-id="3f489-133">상속자</span><span class="sxs-lookup"><span data-stu-id="3f489-133">NOTES</span></span>

## <span data-ttu-id="3f489-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3f489-134">RELATED LINKS</span></span>

