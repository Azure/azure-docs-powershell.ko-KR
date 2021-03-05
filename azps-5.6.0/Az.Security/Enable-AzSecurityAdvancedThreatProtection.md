---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/enable-azsecurityadvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Enable-AzSecurityAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Enable-AzSecurityAdvancedThreatProtection.md
ms.openlocfilehash: 10bda682881f35bc8401bec7304dcc1a68fd1d66
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986594"
---
# <span data-ttu-id="c2ac4-101">Enable-AzSecurityAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="c2ac4-101">Enable-AzSecurityAdvancedThreatProtection</span></span>

## <span data-ttu-id="c2ac4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2ac4-102">SYNOPSIS</span></span>
<span data-ttu-id="c2ac4-103">저장소/cosmosDB 계정에 대한 고급 위협 보호 정책을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2ac4-103">Enables the advanced threat protection policy for a storage / cosmosDB account.</span></span>

## <span data-ttu-id="c2ac4-104">구문</span><span class="sxs-lookup"><span data-stu-id="c2ac4-104">SYNTAX</span></span>

```
Enable-AzSecurityAdvancedThreatProtection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2ac4-105">설명</span><span class="sxs-lookup"><span data-stu-id="c2ac4-105">DESCRIPTION</span></span>
<span data-ttu-id="c2ac4-106">`Enable-AzSecurityAdvancedThreatProtection`cmdlet을 사용하면 저장소/cosmosDB 계정에 대한 위협 보호 정책을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2ac4-106">The `Enable-AzSecurityAdvancedThreatProtection` cmdlet enables the threat protection policy for a storage / cosmosDB account.</span></span>
<span data-ttu-id="c2ac4-107">이 cmdlet을 사용하 는 ResourceId 매개 *변수를* 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c2ac4-107">To use this cmdlet, specify the *ResourceId* parameter.</span></span>

## <span data-ttu-id="c2ac4-108">예제</span><span class="sxs-lookup"><span data-stu-id="c2ac4-108">EXAMPLES</span></span>

### <span data-ttu-id="c2ac4-109">예제 1: Storage 계정</span><span class="sxs-lookup"><span data-stu-id="c2ac4-109">Example 1: Storage Account</span></span>
```powershell
PS C:\> Enable-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"

IsEnabled Id
--------- --
    True  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"
```

<span data-ttu-id="c2ac4-110">이 명령을 사용하면 리소스 ID에 대한 고급 위협 보호 정책을 사용할 수 `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"` 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2ac4-110">This command enables the advanced threat protection policy for resource id `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"`.</span></span>

### <span data-ttu-id="c2ac4-111">예제 2: CosmosDB 계정</span><span class="sxs-lookup"><span data-stu-id="c2ac4-111">Example 2: CosmosDB Account</span></span>
```powershell
PS C:\> Enable-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"

IsEnabled Id
--------- --
    True  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"
```

<span data-ttu-id="c2ac4-112">이 명령을 사용하면 리소스 ID에 대한 고급 위협 보호 정책을 사용할 수 ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"` 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2ac4-112">This command enables the advanced threat protection policy for resource id ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"`.</span></span>

## <span data-ttu-id="c2ac4-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c2ac4-113">PARAMETERS</span></span>

### <span data-ttu-id="c2ac4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2ac4-114">-DefaultProfile</span></span>
<span data-ttu-id="c2ac4-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c2ac4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2ac4-116">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c2ac4-116">-ResourceId</span></span>
<span data-ttu-id="c2ac4-117">명령을 호출할 보안 리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c2ac4-117">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="c2ac4-118">-확인</span><span class="sxs-lookup"><span data-stu-id="c2ac4-118">-Confirm</span></span>
<span data-ttu-id="c2ac4-119">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2ac4-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2ac4-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2ac4-120">-WhatIf</span></span>
<span data-ttu-id="c2ac4-121">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="c2ac4-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c2ac4-122">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c2ac4-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2ac4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2ac4-123">CommonParameters</span></span>
<span data-ttu-id="c2ac4-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c2ac4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2ac4-125">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c2ac4-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2ac4-126">입력</span><span class="sxs-lookup"><span data-stu-id="c2ac4-126">INPUTS</span></span>

### <span data-ttu-id="c2ac4-127">없음</span><span class="sxs-lookup"><span data-stu-id="c2ac4-127">None</span></span>

## <span data-ttu-id="c2ac4-128">출력</span><span class="sxs-lookup"><span data-stu-id="c2ac4-128">OUTPUTS</span></span>

### <span data-ttu-id="c2ac4-129">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="c2ac4-129">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span></span>

## <span data-ttu-id="c2ac4-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c2ac4-130">NOTES</span></span>

## <span data-ttu-id="c2ac4-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c2ac4-131">RELATED LINKS</span></span>
