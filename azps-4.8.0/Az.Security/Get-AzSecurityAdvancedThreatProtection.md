---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/get-azsecurityadvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdvancedThreatProtection.md
ms.openlocfilehash: e4412d770f47bda0de735b315d638c0b8fdb26df
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94203758"
---
# <span data-ttu-id="a9eb6-101">Get-AzSecurityAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="a9eb6-101">Get-AzSecurityAdvancedThreatProtection</span></span>

## <span data-ttu-id="a9eb6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9eb6-102">SYNOPSIS</span></span>
<span data-ttu-id="a9eb6-103">저장소/cosmosDB 계정에 대 한 고급 위협 보호 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a9eb6-103">Gets the advanced threat protection policy for a storage / cosmosDB account.</span></span>

## <span data-ttu-id="a9eb6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a9eb6-104">SYNTAX</span></span>

```
Get-AzSecurityAdvancedThreatProtection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a9eb6-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a9eb6-105">DESCRIPTION</span></span>
<span data-ttu-id="a9eb6-106">`Get-AzSecurityAdvancedThreatProtection`Cmdlet은 저장소/cosmosDB 계정에 대 한 위협 보호 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a9eb6-106">The `Get-AzSecurityAdvancedThreatProtection` cmdlet gets the threat protection policy for a storage / cosmosDB account.</span></span>
<span data-ttu-id="a9eb6-107">이 cmdlet을 사용 하려면 *ResourceId* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9eb6-107">To use this cmdlet, specify the *ResourceId* parameter.</span></span>

## <span data-ttu-id="a9eb6-108">예제의</span><span class="sxs-lookup"><span data-stu-id="a9eb6-108">EXAMPLES</span></span>

### <span data-ttu-id="a9eb6-109">예제 1: 저장소 계정</span><span class="sxs-lookup"><span data-stu-id="a9eb6-109">Example 1: Storage Account</span></span>
```powershell
PS C:\> Get-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"

IsEnabled Id
--------- --
    False  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"
```

<span data-ttu-id="a9eb6-110">이 명령은 리소스 id에 대 한 고급 위협 보호 정책을 가져옵니다 `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"` .</span><span class="sxs-lookup"><span data-stu-id="a9eb6-110">This command gets the advanced threat protection policy for resource id `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"`.</span></span>

### <span data-ttu-id="a9eb6-111">예제 2: CosmosDB Account</span><span class="sxs-lookup"><span data-stu-id="a9eb6-111">Example 2: CosmosDB Account</span></span>
```powershell
PS C:\> Get-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"

IsEnabled Id
--------- --
    True  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"
```

<span data-ttu-id="a9eb6-112">이 명령은 리소스 id에 대 한 고급 위협 보호 정책을 가져옵니다 ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"` .</span><span class="sxs-lookup"><span data-stu-id="a9eb6-112">This command gets the advanced threat protection policy for resource id ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"`.</span></span>

## <span data-ttu-id="a9eb6-113">변수</span><span class="sxs-lookup"><span data-stu-id="a9eb6-113">PARAMETERS</span></span>

### <span data-ttu-id="a9eb6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9eb6-114">-DefaultProfile</span></span>
<span data-ttu-id="a9eb6-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a9eb6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9eb6-116">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a9eb6-116">-ResourceId</span></span>
<span data-ttu-id="a9eb6-117">명령을 호출 하려는 보안 리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a9eb6-117">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="a9eb6-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9eb6-118">CommonParameters</span></span>
<span data-ttu-id="a9eb6-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9eb6-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9eb6-120">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a9eb6-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9eb6-121">입력</span><span class="sxs-lookup"><span data-stu-id="a9eb6-121">INPUTS</span></span>

### <span data-ttu-id="a9eb6-122">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a9eb6-122">System.String</span></span>

## <span data-ttu-id="a9eb6-123">출력</span><span class="sxs-lookup"><span data-stu-id="a9eb6-123">OUTPUTS</span></span>

### <span data-ttu-id="a9eb6-124">AdvancedThreatProtection. PSAdvancedThreatProtection에 대 한 Microsoft</span><span class="sxs-lookup"><span data-stu-id="a9eb6-124">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span></span>

## <span data-ttu-id="a9eb6-125">상속자</span><span class="sxs-lookup"><span data-stu-id="a9eb6-125">NOTES</span></span>

## <span data-ttu-id="a9eb6-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a9eb6-126">RELATED LINKS</span></span>
