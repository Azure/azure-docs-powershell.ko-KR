---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 0DB0B08A-F948-4F6E-9CF0-2FB5DD5064D3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlelasticpoolactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolActivity.md
ms.openlocfilehash: 88052c9f47359e0080e193f5a2dbb1004b48b0e7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702832"
---
# <span data-ttu-id="989af-101">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="989af-101">Get-AzureRmSqlElasticPoolActivity</span></span>

## <span data-ttu-id="989af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="989af-102">SYNOPSIS</span></span>
<span data-ttu-id="989af-103">탄력적 풀에 대 한 작업의 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="989af-103">Gets the status of operations on an elastic pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="989af-104">구문과</span><span class="sxs-lookup"><span data-stu-id="989af-104">SYNTAX</span></span>

```
Get-AzureRmSqlElasticPoolActivity [-ServerName] <String> [-ElasticPoolName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="989af-105">설명은</span><span class="sxs-lookup"><span data-stu-id="989af-105">DESCRIPTION</span></span>
<span data-ttu-id="989af-106">**AzureRmSqlElasticPoolActivity** Cmdlet은 Azure SQL 데이터베이스의 탄력적 풀에 대 한 작업의 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="989af-106">The **Get-AzureRmSqlElasticPoolActivity** cmdlet gets the status of operations on an elastic pool for an Azure SQL Database.</span></span>
<span data-ttu-id="989af-107">풀 만들기 및 구성 업데이트의 상태를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="989af-107">You can see the status of both pool creation and configuration updates.</span></span>

## <span data-ttu-id="989af-108">예제의</span><span class="sxs-lookup"><span data-stu-id="989af-108">EXAMPLES</span></span>

### <span data-ttu-id="989af-109">예제 1: 탄력적 풀에 대 한 작업 상태 가져오기</span><span class="sxs-lookup"><span data-stu-id="989af-109">Example 1: Get the status of operations for an elastic pool</span></span>
```
PS C:\>Get-AzureRmSqlElasticPoolActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="989af-110">이 명령은 ElasticPool01 이라는 탄력적 풀에 대 한 작업의 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="989af-110">This command gets the status of the operations for the elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="989af-111">변수</span><span class="sxs-lookup"><span data-stu-id="989af-111">PARAMETERS</span></span>

### <span data-ttu-id="989af-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="989af-112">-DefaultProfile</span></span>
<span data-ttu-id="989af-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="989af-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="989af-114">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="989af-114">-ElasticPoolName</span></span>
<span data-ttu-id="989af-115">탄력적 풀의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="989af-115">Specifies the name of an elastic pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="989af-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="989af-116">-ResourceGroupName</span></span>
<span data-ttu-id="989af-117">탄력적 풀이 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="989af-117">Specifies the name of a resource group to which the elastic pool is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="989af-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="989af-118">-ServerName</span></span>
<span data-ttu-id="989af-119">탄력적 풀이 포함 된 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="989af-119">Specifies the name of a server that contains an elastic pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="989af-120">-확인</span><span class="sxs-lookup"><span data-stu-id="989af-120">-Confirm</span></span>
<span data-ttu-id="989af-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="989af-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="989af-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="989af-122">-WhatIf</span></span>
<span data-ttu-id="989af-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="989af-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="989af-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="989af-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="989af-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="989af-125">CommonParameters</span></span>
<span data-ttu-id="989af-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="989af-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="989af-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="989af-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="989af-128">입력</span><span class="sxs-lookup"><span data-stu-id="989af-128">INPUTS</span></span>

### <span data-ttu-id="989af-129">않아야</span><span class="sxs-lookup"><span data-stu-id="989af-129">None</span></span>
<span data-ttu-id="989af-130">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="989af-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="989af-131">출력</span><span class="sxs-lookup"><span data-stu-id="989af-131">OUTPUTS</span></span>

### <span data-ttu-id="989af-132">ElasticPool. AzureSqlElasticPoolActivityModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="989af-132">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolActivityModel</span></span>

## <span data-ttu-id="989af-133">상속자</span><span class="sxs-lookup"><span data-stu-id="989af-133">NOTES</span></span>

## <span data-ttu-id="989af-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="989af-134">RELATED LINKS</span></span>

[<span data-ttu-id="989af-135">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="989af-135">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="989af-136">Get-AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="989af-136">Get-AzureRmSqlElasticPoolDatabase</span></span>](./Get-AzureRmSqlElasticPoolDatabase.md)

[<span data-ttu-id="989af-137">새로운 AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="989af-137">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="989af-138">제거-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="989af-138">Remove-AzureRmSqlElasticPool</span></span>](./Remove-AzureRmSqlElasticPool.md)

[<span data-ttu-id="989af-139">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="989af-139">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)


