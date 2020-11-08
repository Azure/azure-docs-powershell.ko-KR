---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Get-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationService.md
ms.openlocfilehash: 287e4db59ae19efec604da9b63958b5ea74b747f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042570"
---
# <span data-ttu-id="bcbc3-101">Get-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="bcbc3-101">Get-AzDataMigrationService</span></span>

## <span data-ttu-id="bcbc3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bcbc3-102">SYNOPSIS</span></span>
<span data-ttu-id="bcbc3-103">Azure 데이터베이스 마이그레이션 서비스의 인스턴스와 연결 된 속성을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="bcbc3-103">Retrieves the properties associated with an instance of the Azure Database Migration Service.</span></span> 

## <span data-ttu-id="bcbc3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bcbc3-104">SYNTAX</span></span>

### <span data-ttu-id="bcbc3-105">ResourceGroupSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="bcbc3-105">ResourceGroupSet (Default)</span></span>
```
Get-AzDataMigrationService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bcbc3-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bcbc3-106">ResourceIdParameterSet</span></span>
```
Get-AzDataMigrationService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bcbc3-107">ServiceNameGroupSet</span><span class="sxs-lookup"><span data-stu-id="bcbc3-107">ServiceNameGroupSet</span></span>
```
Get-AzDataMigrationService [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bcbc3-108">설명은</span><span class="sxs-lookup"><span data-stu-id="bcbc3-108">DESCRIPTION</span></span>
<span data-ttu-id="bcbc3-109">Get-AzDataMigrationService cmdlet은 서비스 이름 및 Azure 리소스 그룹 이름을 기반으로 하는 Azure 데이터베이스 마이그레이션 서비스의 인스턴스와 연결 된 속성을 입력 매개 변수로 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="bcbc3-109">The Get-AzDataMigrationService cmdlet retrieves the properties associated with an instance of the Azure Database Migration Service based on Service name and Azure Resource Group name as input parameters.</span></span> 

## <span data-ttu-id="bcbc3-110">예제의</span><span class="sxs-lookup"><span data-stu-id="bcbc3-110">EXAMPLES</span></span>

### <span data-ttu-id="bcbc3-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="bcbc3-111">Example 1</span></span>
```
PS C:\> Get-AzDataMigrationService -ResourceGroupName testResourceGroup -Name testService
```

<span data-ttu-id="bcbc3-112">위 예제에서는 testService 라는 Azure 데이터베이스 마이그레이션 서비스 인스턴스의 속성을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="bcbc3-112">The above example retrieves the properties of the Azure Database Migration Service instance called testService.</span></span> 

### <span data-ttu-id="bcbc3-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="bcbc3-113">Example 2</span></span>
```
PS C:\> Get-AzDataMigrationService -ResourceGroupName testResourceGroup
```

<span data-ttu-id="bcbc3-114">위 예제에서는 testResourceGroup 이라는 리소스 그룹에서 Azure 데이터베이스 마이그레이션 서비스를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="bcbc3-114">The above example retrieves Azure Database Migration Services in the resource group called testResourceGroup.</span></span> 

## <span data-ttu-id="bcbc3-115">변수</span><span class="sxs-lookup"><span data-stu-id="bcbc3-115">PARAMETERS</span></span>

### <span data-ttu-id="bcbc3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcbc3-116">-DefaultProfile</span></span>
<span data-ttu-id="bcbc3-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bcbc3-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bcbc3-118">-이름</span><span class="sxs-lookup"><span data-stu-id="bcbc3-118">-Name</span></span>
<span data-ttu-id="bcbc3-119">데이터베이스 마이그레이션 서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bcbc3-119">Name of Database Migration Service.</span></span>

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

### <span data-ttu-id="bcbc3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcbc3-120">-ResourceGroupName</span></span>
<span data-ttu-id="bcbc3-121">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bcbc3-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="bcbc3-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bcbc3-122">-ResourceId</span></span>
<span data-ttu-id="bcbc3-123">DataMigrationService 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="bcbc3-123">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="bcbc3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcbc3-124">CommonParameters</span></span>
<span data-ttu-id="bcbc3-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bcbc3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcbc3-126">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bcbc3-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcbc3-127">입력</span><span class="sxs-lookup"><span data-stu-id="bcbc3-127">INPUTS</span></span>

### <span data-ttu-id="bcbc3-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="bcbc3-128">System.String</span></span>

## <span data-ttu-id="bcbc3-129">출력</span><span class="sxs-lookup"><span data-stu-id="bcbc3-129">OUTPUTS</span></span>

### <span data-ttu-id="bcbc3-130">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="bcbc3-130">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

## <span data-ttu-id="bcbc3-131">상속자</span><span class="sxs-lookup"><span data-stu-id="bcbc3-131">NOTES</span></span>

## <span data-ttu-id="bcbc3-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bcbc3-132">RELATED LINKS</span></span>
