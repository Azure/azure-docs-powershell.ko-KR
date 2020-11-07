---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Get-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationService.md
ms.openlocfilehash: dcb9d6e58a743f37aa71d91b0b73772c239f252e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868474"
---
# <span data-ttu-id="b4a2d-101">Get-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="b4a2d-101">Get-AzDataMigrationService</span></span>

## <span data-ttu-id="b4a2d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4a2d-102">SYNOPSIS</span></span>
<span data-ttu-id="b4a2d-103">Azure 데이터베이스 마이그레이션 서비스의 인스턴스와 연결 된 속성을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4a2d-103">Retrieves the properties associated with an instance of the Azure Database Migration Service.</span></span> 

## <span data-ttu-id="b4a2d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b4a2d-104">SYNTAX</span></span>

### <span data-ttu-id="b4a2d-105">ResourceGroupSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="b4a2d-105">ResourceGroupSet (Default)</span></span>
```
Get-AzDataMigrationService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b4a2d-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4a2d-106">ResourceIdParameterSet</span></span>
```
Get-AzDataMigrationService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b4a2d-107">ServiceNameGroupSet</span><span class="sxs-lookup"><span data-stu-id="b4a2d-107">ServiceNameGroupSet</span></span>
```
Get-AzDataMigrationService [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4a2d-108">설명은</span><span class="sxs-lookup"><span data-stu-id="b4a2d-108">DESCRIPTION</span></span>
<span data-ttu-id="b4a2d-109">Get-AzDataMigrationService cmdlet은 서비스 이름 및 Azure 리소스 그룹 이름을 기반으로 하는 Azure 데이터베이스 마이그레이션 서비스의 인스턴스와 연결 된 속성을 입력 매개 변수로 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4a2d-109">The Get-AzDataMigrationService cmdlet retrieves the properties associated with an instance of the Azure Database Migration Service based on Service name and Azure Resource Group name as input parameters.</span></span> 

## <span data-ttu-id="b4a2d-110">예제의</span><span class="sxs-lookup"><span data-stu-id="b4a2d-110">EXAMPLES</span></span>

### <span data-ttu-id="b4a2d-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="b4a2d-111">Example 1</span></span>
```
PS C:\> Get-AzDataMigrationService -ResourceGroupName testResourceGroup -Name testService
```

<span data-ttu-id="b4a2d-112">위 예제에서는 testService 라는 Azure 데이터베이스 마이그레이션 서비스 인스턴스의 속성을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4a2d-112">The above example retrieves the properties of the Azure Database Migration Service instance called testService.</span></span> 

### <span data-ttu-id="b4a2d-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="b4a2d-113">Example 2</span></span>
```
PS C:\> Get-AzDataMigrationService -ResourceGroupName testResourceGroup
```

<span data-ttu-id="b4a2d-114">위 예제에서는 testResourceGroup 이라는 리소스 그룹에서 Azure 데이터베이스 마이그레이션 서비스를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4a2d-114">The above example retrieves Azure Database Migration Services in the resource group called testResourceGroup.</span></span> 

## <span data-ttu-id="b4a2d-115">변수</span><span class="sxs-lookup"><span data-stu-id="b4a2d-115">PARAMETERS</span></span>

### <span data-ttu-id="b4a2d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4a2d-116">-DefaultProfile</span></span>
<span data-ttu-id="b4a2d-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b4a2d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4a2d-118">-이름</span><span class="sxs-lookup"><span data-stu-id="b4a2d-118">-Name</span></span>
<span data-ttu-id="b4a2d-119">데이터베이스 마이그레이션 서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b4a2d-119">Name of Database Migration Service.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameGroupSet
Aliases: ServiceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4a2d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4a2d-120">-ResourceGroupName</span></span>
<span data-ttu-id="b4a2d-121">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b4a2d-121">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ServiceNameGroupSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4a2d-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b4a2d-122">-ResourceId</span></span>
<span data-ttu-id="b4a2d-123">DataMigrationService 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="b4a2d-123">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="b4a2d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4a2d-124">CommonParameters</span></span>
<span data-ttu-id="b4a2d-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4a2d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4a2d-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4a2d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4a2d-127">입력</span><span class="sxs-lookup"><span data-stu-id="b4a2d-127">INPUTS</span></span>

### <span data-ttu-id="b4a2d-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b4a2d-128">System.String</span></span>

## <span data-ttu-id="b4a2d-129">출력</span><span class="sxs-lookup"><span data-stu-id="b4a2d-129">OUTPUTS</span></span>

### <span data-ttu-id="b4a2d-130">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="b4a2d-130">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

## <span data-ttu-id="b4a2d-131">상속자</span><span class="sxs-lookup"><span data-stu-id="b4a2d-131">NOTES</span></span>

## <span data-ttu-id="b4a2d-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b4a2d-132">RELATED LINKS</span></span>
