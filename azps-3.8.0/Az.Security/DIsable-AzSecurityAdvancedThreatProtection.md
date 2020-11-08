---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/disable-azsecurityadvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/DIsable-AzSecurityAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/DIsable-AzSecurityAdvancedThreatProtection.md
ms.openlocfilehash: 28e8521a283362989ff3ebace2f1e0a3e32c17a7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043480"
---
# <span data-ttu-id="2ed13-101">Disable-AzSecurityAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="2ed13-101">Disable-AzSecurityAdvancedThreatProtection</span></span>

## <span data-ttu-id="2ed13-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ed13-102">SYNOPSIS</span></span>
<span data-ttu-id="2ed13-103">저장소/cosmosDB 계정에 대 한 고급 위협 보호 정책을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ed13-103">Disables the advanced threat protection policy for a storage / cosmosDB account.</span></span>

## <span data-ttu-id="2ed13-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2ed13-104">SYNTAX</span></span>

```
Disable-AzSecurityAdvancedThreatProtection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ed13-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2ed13-105">DESCRIPTION</span></span>
<span data-ttu-id="2ed13-106">`Disable-AzSecurityAdvancedThreatProtection`Cmdlet은 저장소/cosmosDB 계정에 대 한 위협 보호 정책을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ed13-106">The `Disable-AzSecurityAdvancedThreatProtection` cmdlet disables the threat protection policy for a storage / cosmosDB account.</span></span>
<span data-ttu-id="2ed13-107">이 cmdlet을 사용 하려면 *ResourceId* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ed13-107">To use this cmdlet, specify the *ResourceId* parameter.</span></span>

## <span data-ttu-id="2ed13-108">예제의</span><span class="sxs-lookup"><span data-stu-id="2ed13-108">EXAMPLES</span></span>

### <span data-ttu-id="2ed13-109">예제 1: 저장소 계정</span><span class="sxs-lookup"><span data-stu-id="2ed13-109">Example 1 : Storage Account</span></span>
```powershell
PS C:\> Disable-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"

IsEnabled Id
--------- --
    False  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"
```

<span data-ttu-id="2ed13-110">이 명령은 리소스 id에 대 한 고급 위협 보호 정책을 사용 하지 않도록 설정 합니다 `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"` .</span><span class="sxs-lookup"><span data-stu-id="2ed13-110">This command disables the advanced threat protection policy for resource id `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"`.</span></span>

### <span data-ttu-id="2ed13-111">예제 2: CosmosDB Account</span><span class="sxs-lookup"><span data-stu-id="2ed13-111">Example 2 : CosmosDB Account</span></span>
```powershell
PS C:\> Disable-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"

IsEnabled Id
--------- --
    False  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"
```
<span data-ttu-id="2ed13-112">이 명령은 리소스 id에 대 한 고급 위협 보호 정책을 사용 하지 않도록 설정 합니다 ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"` .</span><span class="sxs-lookup"><span data-stu-id="2ed13-112">This command disables the advanced threat protection policy for resource id ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"`.</span></span>


## <span data-ttu-id="2ed13-113">변수</span><span class="sxs-lookup"><span data-stu-id="2ed13-113">PARAMETERS</span></span>

### <span data-ttu-id="2ed13-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ed13-114">-DefaultProfile</span></span>
<span data-ttu-id="2ed13-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2ed13-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ed13-116">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2ed13-116">-ResourceId</span></span>
<span data-ttu-id="2ed13-117">명령을 호출 하려는 보안 리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="2ed13-117">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="2ed13-118">-확인</span><span class="sxs-lookup"><span data-stu-id="2ed13-118">-Confirm</span></span>
<span data-ttu-id="2ed13-119">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ed13-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ed13-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ed13-120">-WhatIf</span></span>
<span data-ttu-id="2ed13-121">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2ed13-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2ed13-122">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2ed13-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ed13-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ed13-123">CommonParameters</span></span>
<span data-ttu-id="2ed13-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ed13-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ed13-125">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ed13-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ed13-126">입력</span><span class="sxs-lookup"><span data-stu-id="2ed13-126">INPUTS</span></span>

### <span data-ttu-id="2ed13-127">않아야</span><span class="sxs-lookup"><span data-stu-id="2ed13-127">None</span></span>

## <span data-ttu-id="2ed13-128">출력</span><span class="sxs-lookup"><span data-stu-id="2ed13-128">OUTPUTS</span></span>

### <span data-ttu-id="2ed13-129">AdvancedThreatProtection. PSAdvancedThreatProtection에 대 한 Microsoft</span><span class="sxs-lookup"><span data-stu-id="2ed13-129">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span></span>

## <span data-ttu-id="2ed13-130">상속자</span><span class="sxs-lookup"><span data-stu-id="2ed13-130">NOTES</span></span>

## <span data-ttu-id="2ed13-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2ed13-131">RELATED LINKS</span></span>
