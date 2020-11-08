---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqluniquekeypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKeyPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKeyPolicy.md
ms.openlocfilehash: bf91d1948b4040a35ee77f2a1111861a03076783
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212865"
---
# <span data-ttu-id="8aa3a-101">New-AzCosmosDBSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="8aa3a-101">New-AzCosmosDBSqlUniqueKeyPolicy</span></span>

## <span data-ttu-id="8aa3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8aa3a-102">SYNOPSIS</span></span>
<span data-ttu-id="8aa3a-103">새 CosmosDB SqlUniqueKeyPolicy 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8aa3a-103">Creates a new CosmosDB SqlUniqueKeyPolicy object.</span></span>

## <span data-ttu-id="8aa3a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8aa3a-104">SYNTAX</span></span>

```
New-AzCosmosDBSqlUniqueKeyPolicy -UniqueKey <PSSqlUniqueKey[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8aa3a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8aa3a-105">DESCRIPTION</span></span>
<span data-ttu-id="8aa3a-106">**AzCosmosDBSqlUniqueKeyPolicy** Cmdlet은 PSSqlUniqueKeyPolicy 유형의 새 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8aa3a-106">The **New-AzCosmosDBSqlUniqueKeyPolicy** cmdlet creates a new object of type PSSqlUniqueKeyPolicy.</span></span>

## <span data-ttu-id="8aa3a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8aa3a-107">EXAMPLES</span></span>

### <span data-ttu-id="8aa3a-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="8aa3a-108">Example 1</span></span>
```powershell
PS C:\>New-AzCosmosDBSqlUniqueKeyPolicy -UniqueKey {psUniqueKey1, psUniqueKey2}

UniqueKey
---------
{Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey, Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey}
```

## <span data-ttu-id="8aa3a-109">변수</span><span class="sxs-lookup"><span data-stu-id="8aa3a-109">PARAMETERS</span></span>

### <span data-ttu-id="8aa3a-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8aa3a-110">-DefaultProfile</span></span>
<span data-ttu-id="8aa3a-111">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8aa3a-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8aa3a-112">-UniqueKey</span><span class="sxs-lookup"><span data-stu-id="8aa3a-112">-UniqueKey</span></span>
<span data-ttu-id="8aa3a-113">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8aa3a-113">Database name.</span></span>

```yaml
Type: PSSqlUniqueKey[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8aa3a-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8aa3a-114">CommonParameters</span></span>
<span data-ttu-id="8aa3a-115">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8aa3a-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8aa3a-116">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8aa3a-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8aa3a-117">입력</span><span class="sxs-lookup"><span data-stu-id="8aa3a-117">INPUTS</span></span>

### <span data-ttu-id="8aa3a-118">않아야</span><span class="sxs-lookup"><span data-stu-id="8aa3a-118">None</span></span>

## <span data-ttu-id="8aa3a-119">출력</span><span class="sxs-lookup"><span data-stu-id="8aa3a-119">OUTPUTS</span></span>

### <span data-ttu-id="8aa3a-120">CosmosDB. PSSqlUniqueKeyPolicy/.</span><span class="sxs-lookup"><span data-stu-id="8aa3a-120">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span></span>

## <span data-ttu-id="8aa3a-121">상속자</span><span class="sxs-lookup"><span data-stu-id="8aa3a-121">NOTES</span></span>

## <span data-ttu-id="8aa3a-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8aa3a-122">RELATED LINKS</span></span>
