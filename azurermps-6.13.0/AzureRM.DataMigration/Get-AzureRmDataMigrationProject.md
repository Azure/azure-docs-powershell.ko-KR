---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/Get-AzureRmDataMigrationProject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationProject.md
ms.openlocfilehash: 31d37f740500247fed433c3e40b9d8220a5af663
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532015"
---
# <span data-ttu-id="93bf0-101">Get-AzureRmDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="93bf0-101">Get-AzureRmDataMigrationProject</span></span>

## <span data-ttu-id="93bf0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93bf0-102">SYNOPSIS</span></span>
<span data-ttu-id="93bf0-103">Azure 데이터베이스 마이그레이션 프로젝트의 속성을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="93bf0-103">Retrieves the properties of an Azure Database Migration project.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="93bf0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="93bf0-104">SYNTAX</span></span>

### <span data-ttu-id="93bf0-105">ComponentNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="93bf0-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzureRmDataMigrationProject -ResourceGroupName <String> -ServiceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="93bf0-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="93bf0-106">ComponentObjectParameterSet</span></span>
```
Get-AzureRmDataMigrationProject [-InputObject] <PSDataMigrationService> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="93bf0-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="93bf0-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmDataMigrationProject [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93bf0-108">설명은</span><span class="sxs-lookup"><span data-stu-id="93bf0-108">DESCRIPTION</span></span>
<span data-ttu-id="93bf0-109">Get-AzureRmDataMigrationProject cmdlet은 Azure 데이터베이스 마이그레이션 프로젝트의 속성을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="93bf0-109">The Get-AzureRmDataMigrationProject cmdlet retrieves the properties of an Azure Database Migration project.</span></span>

## <span data-ttu-id="93bf0-110">예제의</span><span class="sxs-lookup"><span data-stu-id="93bf0-110">EXAMPLES</span></span>

### <span data-ttu-id="93bf0-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="93bf0-111">Example 1</span></span>
```
PS C:\> Get-AzureRmDataMigrationProject -ServiceName testService -Name testProject -ResourceGroup testResourceGroup
```

<span data-ttu-id="93bf0-112">위 예제에서는 리소스 그룹에서 testResourceGroup 이라는 TestProject 이라는 Azure 데이터베이스 마이그레이션 프로젝트를 검색 하 고 서비스에서 Testresourcegroup 라는 서비스로</span><span class="sxs-lookup"><span data-stu-id="93bf0-112">The above example retrieves  Azure Database Migration project named TestProject in the resource group called testResourceGroup and under service called testService</span></span>

### <span data-ttu-id="93bf0-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="93bf0-113">Example 2</span></span>
```
PS C:\> Get-AzureRmDataMigrationProject -InputObject $myService
```

<span data-ttu-id="93bf0-114">위 예제에서는 전달 된 PSProject 개체 입력 매개 변수를 기반으로 Azure 데이터베이스 마이그레이션 프로젝트를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="93bf0-114">The above example retrieves the  Azure Database Migration project based on PSProject object input parameter passed in.</span></span> 

## <span data-ttu-id="93bf0-115">변수</span><span class="sxs-lookup"><span data-stu-id="93bf0-115">PARAMETERS</span></span>

### <span data-ttu-id="93bf0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93bf0-116">-DefaultProfile</span></span>
<span data-ttu-id="93bf0-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="93bf0-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="93bf0-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="93bf0-118">-InputObject</span></span>
<span data-ttu-id="93bf0-119">PSDataMigrationService 개체</span><span class="sxs-lookup"><span data-stu-id="93bf0-119">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="93bf0-120">-이름</span><span class="sxs-lookup"><span data-stu-id="93bf0-120">-Name</span></span>
<span data-ttu-id="93bf0-121">프로젝트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="93bf0-121">The name of the project.</span></span>

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

### <span data-ttu-id="93bf0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93bf0-122">-ResourceGroupName</span></span>
<span data-ttu-id="93bf0-123">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="93bf0-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="93bf0-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="93bf0-124">-ResourceId</span></span>
<span data-ttu-id="93bf0-125">DataMigrationService 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="93bf0-125">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="93bf0-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="93bf0-126">-ServiceName</span></span>
<span data-ttu-id="93bf0-127">데이터베이스 마이그레이션 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="93bf0-127">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="93bf0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93bf0-128">CommonParameters</span></span>
<span data-ttu-id="93bf0-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="93bf0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93bf0-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93bf0-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93bf0-131">입력</span><span class="sxs-lookup"><span data-stu-id="93bf0-131">INPUTS</span></span>

### <span data-ttu-id="93bf0-132">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="93bf0-132">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>
<span data-ttu-id="93bf0-133">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="93bf0-133">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="93bf0-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="93bf0-134">System.String</span></span>

## <span data-ttu-id="93bf0-135">출력</span><span class="sxs-lookup"><span data-stu-id="93bf0-135">OUTPUTS</span></span>

### <span data-ttu-id="93bf0-136">DataMigration. a i m. PSProject</span><span class="sxs-lookup"><span data-stu-id="93bf0-136">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

## <span data-ttu-id="93bf0-137">상속자</span><span class="sxs-lookup"><span data-stu-id="93bf0-137">NOTES</span></span>

## <span data-ttu-id="93bf0-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="93bf0-138">RELATED LINKS</span></span>
