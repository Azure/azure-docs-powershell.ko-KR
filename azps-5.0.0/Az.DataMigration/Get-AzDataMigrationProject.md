---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Get-AzDataMigrationProject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationProject.md
ms.openlocfilehash: 7fe1e12c7c7feb2a47ac33b309b188e53e77fc73
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94305453"
---
# <span data-ttu-id="7a68f-101">Get-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="7a68f-101">Get-AzDataMigrationProject</span></span>

## <span data-ttu-id="7a68f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a68f-102">SYNOPSIS</span></span>
<span data-ttu-id="7a68f-103">Azure 데이터베이스 마이그레이션 프로젝트의 속성을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a68f-103">Retrieves the properties of an Azure Database Migration project.</span></span>

## <span data-ttu-id="7a68f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7a68f-104">SYNTAX</span></span>

### <span data-ttu-id="7a68f-105">ComponentNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="7a68f-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzDataMigrationProject -ResourceGroupName <String> -ServiceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7a68f-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a68f-106">ComponentObjectParameterSet</span></span>
```
Get-AzDataMigrationProject [-InputObject] <PSDataMigrationService> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7a68f-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a68f-107">ResourceIdParameterSet</span></span>
```
Get-AzDataMigrationProject [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7a68f-108">설명은</span><span class="sxs-lookup"><span data-stu-id="7a68f-108">DESCRIPTION</span></span>
<span data-ttu-id="7a68f-109">Get-AzDataMigrationProject cmdlet은 Azure 데이터베이스 마이그레이션 프로젝트의 속성을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a68f-109">The Get-AzDataMigrationProject cmdlet retrieves the properties of an Azure Database Migration project.</span></span>

## <span data-ttu-id="7a68f-110">예제의</span><span class="sxs-lookup"><span data-stu-id="7a68f-110">EXAMPLES</span></span>

### <span data-ttu-id="7a68f-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="7a68f-111">Example 1</span></span>
```
PS C:\> Get-AzDataMigrationProject -ServiceName testService -Name testProject -ResourceGroup testResourceGroup
```

<span data-ttu-id="7a68f-112">위 예제에서는 리소스 그룹에서 testResourceGroup 이라는 TestProject 이라는 Azure 데이터베이스 마이그레이션 프로젝트를 검색 하 고 서비스에서 Testresourcegroup 라는 서비스로</span><span class="sxs-lookup"><span data-stu-id="7a68f-112">The above example retrieves  Azure Database Migration project named TestProject in the resource group called testResourceGroup and under service called testService</span></span>

### <span data-ttu-id="7a68f-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="7a68f-113">Example 2</span></span>
```
PS C:\> Get-AzDataMigrationProject -InputObject $myService
```

<span data-ttu-id="7a68f-114">위 예제에서는 전달 된 PSProject 개체 입력 매개 변수를 기반으로 Azure 데이터베이스 마이그레이션 프로젝트를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a68f-114">The above example retrieves the  Azure Database Migration project based on PSProject object input parameter passed in.</span></span> 

## <span data-ttu-id="7a68f-115">변수</span><span class="sxs-lookup"><span data-stu-id="7a68f-115">PARAMETERS</span></span>

### <span data-ttu-id="7a68f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a68f-116">-DefaultProfile</span></span>
<span data-ttu-id="7a68f-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7a68f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7a68f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7a68f-118">-InputObject</span></span>
<span data-ttu-id="7a68f-119">PSDataMigrationService 개체</span><span class="sxs-lookup"><span data-stu-id="7a68f-119">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="7a68f-120">-이름</span><span class="sxs-lookup"><span data-stu-id="7a68f-120">-Name</span></span>
<span data-ttu-id="7a68f-121">프로젝트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7a68f-121">The name of the project.</span></span>

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

### <span data-ttu-id="7a68f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a68f-122">-ResourceGroupName</span></span>
<span data-ttu-id="7a68f-123">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7a68f-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="7a68f-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7a68f-124">-ResourceId</span></span>
<span data-ttu-id="7a68f-125">DataMigrationService 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="7a68f-125">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="7a68f-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="7a68f-126">-ServiceName</span></span>
<span data-ttu-id="7a68f-127">데이터베이스 마이그레이션 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7a68f-127">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="7a68f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a68f-128">CommonParameters</span></span>
<span data-ttu-id="7a68f-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a68f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a68f-130">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a68f-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a68f-131">입력</span><span class="sxs-lookup"><span data-stu-id="7a68f-131">INPUTS</span></span>

### <span data-ttu-id="7a68f-132">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="7a68f-132">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="7a68f-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7a68f-133">System.String</span></span>

## <span data-ttu-id="7a68f-134">출력</span><span class="sxs-lookup"><span data-stu-id="7a68f-134">OUTPUTS</span></span>

### <span data-ttu-id="7a68f-135">DataMigration. a i m. PSProject</span><span class="sxs-lookup"><span data-stu-id="7a68f-135">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

## <span data-ttu-id="7a68f-136">상속자</span><span class="sxs-lookup"><span data-stu-id="7a68f-136">NOTES</span></span>

## <span data-ttu-id="7a68f-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7a68f-137">RELATED LINKS</span></span>
