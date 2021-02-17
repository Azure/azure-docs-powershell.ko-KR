---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/get-azsecurityadvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdvancedThreatProtection.md
ms.openlocfilehash: e4412d770f47bda0de735b315d638c0b8fdb26df
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208336"
---
# <span data-ttu-id="1abde-101">Get-AzSecurityAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="1abde-101">Get-AzSecurityAdvancedThreatProtection</span></span>

## <span data-ttu-id="1abde-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1abde-102">SYNOPSIS</span></span>
<span data-ttu-id="1abde-103">저장소/cosmosDB 계정에 대한 고급 위협 보호 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1abde-103">Gets the advanced threat protection policy for a storage / cosmosDB account.</span></span>

## <span data-ttu-id="1abde-104">구문</span><span class="sxs-lookup"><span data-stu-id="1abde-104">SYNTAX</span></span>

```
Get-AzSecurityAdvancedThreatProtection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1abde-105">설명</span><span class="sxs-lookup"><span data-stu-id="1abde-105">DESCRIPTION</span></span>
<span data-ttu-id="1abde-106">`Get-AzSecurityAdvancedThreatProtection`cmdlet은 저장소/cosmosDB 계정에 대한 위협 보호 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1abde-106">The `Get-AzSecurityAdvancedThreatProtection` cmdlet gets the threat protection policy for a storage / cosmosDB account.</span></span>
<span data-ttu-id="1abde-107">이 cmdlet을 사용 설정하기 위해 ResourceId 매개 *변수를 지정합니다.*</span><span class="sxs-lookup"><span data-stu-id="1abde-107">To use this cmdlet, specify the *ResourceId* parameter.</span></span>

## <span data-ttu-id="1abde-108">예제</span><span class="sxs-lookup"><span data-stu-id="1abde-108">EXAMPLES</span></span>

### <span data-ttu-id="1abde-109">예제 1: Storage 계정</span><span class="sxs-lookup"><span data-stu-id="1abde-109">Example 1: Storage Account</span></span>
```powershell
PS C:\> Get-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"

IsEnabled Id
--------- --
    False  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"
```

<span data-ttu-id="1abde-110">이 명령은 리소스 ID에 대한 고급 위협 보호 정책을 `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"` 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1abde-110">This command gets the advanced threat protection policy for resource id `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"`.</span></span>

### <span data-ttu-id="1abde-111">예제 2: CosmosDB 계정</span><span class="sxs-lookup"><span data-stu-id="1abde-111">Example 2: CosmosDB Account</span></span>
```powershell
PS C:\> Get-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"

IsEnabled Id
--------- --
    True  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"
```

<span data-ttu-id="1abde-112">이 명령은 리소스 ID에 대한 고급 위협 보호 정책을 ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"` 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1abde-112">This command gets the advanced threat protection policy for resource id ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"`.</span></span>

## <span data-ttu-id="1abde-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1abde-113">PARAMETERS</span></span>

### <span data-ttu-id="1abde-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1abde-114">-DefaultProfile</span></span>
<span data-ttu-id="1abde-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1abde-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1abde-116">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1abde-116">-ResourceId</span></span>
<span data-ttu-id="1abde-117">명령을 호출하려는 보안 리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="1abde-117">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="1abde-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1abde-118">CommonParameters</span></span>
<span data-ttu-id="1abde-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1abde-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1abde-120">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1abde-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1abde-121">입력</span><span class="sxs-lookup"><span data-stu-id="1abde-121">INPUTS</span></span>

### <span data-ttu-id="1abde-122">System.String</span><span class="sxs-lookup"><span data-stu-id="1abde-122">System.String</span></span>

## <span data-ttu-id="1abde-123">출력</span><span class="sxs-lookup"><span data-stu-id="1abde-123">OUTPUTS</span></span>

### <span data-ttu-id="1abde-124">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="1abde-124">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span></span>

## <span data-ttu-id="1abde-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1abde-125">NOTES</span></span>

## <span data-ttu-id="1abde-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1abde-126">RELATED LINKS</span></span>
