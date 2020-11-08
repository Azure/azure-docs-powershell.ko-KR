---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/get-azsecurityadvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdvancedThreatProtection.md
ms.openlocfilehash: d4d2ae2ae8b09f319efe2f77030c88338b4c40b9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044307"
---
# <span data-ttu-id="92143-101">Get-AzSecurityAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="92143-101">Get-AzSecurityAdvancedThreatProtection</span></span>

## <span data-ttu-id="92143-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92143-102">SYNOPSIS</span></span>
<span data-ttu-id="92143-103">저장소/cosmosDB 계정에 대 한 고급 위협 보호 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="92143-103">Gets the advanced threat protection policy for a storage / cosmosDB account.</span></span>

## <span data-ttu-id="92143-104">구문과</span><span class="sxs-lookup"><span data-stu-id="92143-104">SYNTAX</span></span>

```
Get-AzSecurityAdvancedThreatProtection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="92143-105">설명은</span><span class="sxs-lookup"><span data-stu-id="92143-105">DESCRIPTION</span></span>
<span data-ttu-id="92143-106">`Get-AzSecurityAdvancedThreatProtection`Cmdlet은 저장소/cosmosDB 계정에 대 한 위협 보호 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="92143-106">The `Get-AzSecurityAdvancedThreatProtection` cmdlet gets the threat protection policy for a storage / cosmosDB account.</span></span>
<span data-ttu-id="92143-107">이 cmdlet을 사용 하려면 *ResourceId* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="92143-107">To use this cmdlet, specify the *ResourceId* parameter.</span></span>

## <span data-ttu-id="92143-108">예제의</span><span class="sxs-lookup"><span data-stu-id="92143-108">EXAMPLES</span></span>

### <span data-ttu-id="92143-109">예제 1: 저장소 계정</span><span class="sxs-lookup"><span data-stu-id="92143-109">Example 1 : Storage Account</span></span>
```powershell
PS C:\> Get-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"

IsEnabled Id
--------- --
    False  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"
```

<span data-ttu-id="92143-110">이 명령은 리소스 id에 대 한 고급 위협 보호 정책을 가져옵니다 `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"` .</span><span class="sxs-lookup"><span data-stu-id="92143-110">This command gets the advanced threat protection policy for resource id `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"`.</span></span>

### <span data-ttu-id="92143-111">예제 2: CosmosDB Account</span><span class="sxs-lookup"><span data-stu-id="92143-111">Example 2 : CosmosDB Account</span></span>
```powershell
PS C:\> Get-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"

IsEnabled Id
--------- --
    True  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"
```
<span data-ttu-id="92143-112">이 명령은 리소스 id에 대 한 고급 위협 보호 정책을 가져옵니다 ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"` .</span><span class="sxs-lookup"><span data-stu-id="92143-112">This command gets the advanced threat protection policy for resource id ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"`.</span></span>


## <span data-ttu-id="92143-113">변수</span><span class="sxs-lookup"><span data-stu-id="92143-113">PARAMETERS</span></span>

### <span data-ttu-id="92143-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92143-114">-DefaultProfile</span></span>
<span data-ttu-id="92143-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="92143-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92143-116">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="92143-116">-ResourceId</span></span>
<span data-ttu-id="92143-117">명령을 호출 하려는 보안 리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="92143-117">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92143-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92143-118">CommonParameters</span></span>
<span data-ttu-id="92143-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="92143-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92143-120">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92143-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92143-121">입력</span><span class="sxs-lookup"><span data-stu-id="92143-121">INPUTS</span></span>

### <span data-ttu-id="92143-122">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="92143-122">System.String</span></span>

## <span data-ttu-id="92143-123">출력</span><span class="sxs-lookup"><span data-stu-id="92143-123">OUTPUTS</span></span>

### <span data-ttu-id="92143-124">AdvancedThreatProtection. PSAdvancedThreatProtection에 대 한 Microsoft</span><span class="sxs-lookup"><span data-stu-id="92143-124">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span></span>

## <span data-ttu-id="92143-125">상속자</span><span class="sxs-lookup"><span data-stu-id="92143-125">NOTES</span></span>

## <span data-ttu-id="92143-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="92143-126">RELATED LINKS</span></span>
