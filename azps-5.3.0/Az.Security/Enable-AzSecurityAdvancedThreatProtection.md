---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/enable-azsecurityadvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Enable-AzSecurityAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Enable-AzSecurityAdvancedThreatProtection.md
ms.openlocfilehash: 3db63fad33fe49fe7aa001f13759e41e7cd7c856
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495048"
---
# <span data-ttu-id="f4c6e-101">Enable-AzSecurityAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="f4c6e-101">Enable-AzSecurityAdvancedThreatProtection</span></span>

## <span data-ttu-id="f4c6e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4c6e-102">SYNOPSIS</span></span>
<span data-ttu-id="f4c6e-103">저장소/cosmosDB 계정에 대한 고급 위협 보호 정책을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f4c6e-103">Enables the advanced threat protection policy for a storage / cosmosDB account.</span></span>

## <span data-ttu-id="f4c6e-104">구문</span><span class="sxs-lookup"><span data-stu-id="f4c6e-104">SYNTAX</span></span>

```
Enable-AzSecurityAdvancedThreatProtection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4c6e-105">설명</span><span class="sxs-lookup"><span data-stu-id="f4c6e-105">DESCRIPTION</span></span>
<span data-ttu-id="f4c6e-106">`Enable-AzSecurityAdvancedThreatProtection`cmdlet을 사용하면 저장소/cosmosDB 계정에 대한 위협 보호 정책을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f4c6e-106">The `Enable-AzSecurityAdvancedThreatProtection` cmdlet enables the threat protection policy for a storage / cosmosDB account.</span></span>
<span data-ttu-id="f4c6e-107">이 cmdlet을 사용 설정하기 위해 ResourceId 매개 *변수를 지정합니다.*</span><span class="sxs-lookup"><span data-stu-id="f4c6e-107">To use this cmdlet, specify the *ResourceId* parameter.</span></span>

## <span data-ttu-id="f4c6e-108">예제</span><span class="sxs-lookup"><span data-stu-id="f4c6e-108">EXAMPLES</span></span>

### <span data-ttu-id="f4c6e-109">예제 1: Storage 계정</span><span class="sxs-lookup"><span data-stu-id="f4c6e-109">Example 1: Storage Account</span></span>
```powershell
PS C:\> Enable-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"

IsEnabled Id
--------- --
    True  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"
```

<span data-ttu-id="f4c6e-110">이 명령을 사용하면 리소스 ID에 대한 고급 위협 보호 정책을 사용할 수 `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"` 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f4c6e-110">This command enables the advanced threat protection policy for resource id `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"`.</span></span>

### <span data-ttu-id="f4c6e-111">예제 2: CosmosDB 계정</span><span class="sxs-lookup"><span data-stu-id="f4c6e-111">Example 2: CosmosDB Account</span></span>
```powershell
PS C:\> Enable-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"

IsEnabled Id
--------- --
    True  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"
```

<span data-ttu-id="f4c6e-112">이 명령을 사용하면 리소스 ID에 대한 고급 위협 보호 정책을 사용할 수 ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"` 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f4c6e-112">This command enables the advanced threat protection policy for resource id ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"`.</span></span>

## <span data-ttu-id="f4c6e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f4c6e-113">PARAMETERS</span></span>

### <span data-ttu-id="f4c6e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4c6e-114">-DefaultProfile</span></span>
<span data-ttu-id="f4c6e-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f4c6e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4c6e-116">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f4c6e-116">-ResourceId</span></span>
<span data-ttu-id="f4c6e-117">명령을 호출하려는 보안 리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="f4c6e-117">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="f4c6e-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f4c6e-118">-Confirm</span></span>
<span data-ttu-id="f4c6e-119">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f4c6e-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4c6e-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4c6e-120">-WhatIf</span></span>
<span data-ttu-id="f4c6e-121">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="f4c6e-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f4c6e-122">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f4c6e-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4c6e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4c6e-123">CommonParameters</span></span>
<span data-ttu-id="f4c6e-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f4c6e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4c6e-125">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f4c6e-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4c6e-126">입력</span><span class="sxs-lookup"><span data-stu-id="f4c6e-126">INPUTS</span></span>

### <span data-ttu-id="f4c6e-127">없음</span><span class="sxs-lookup"><span data-stu-id="f4c6e-127">None</span></span>

## <span data-ttu-id="f4c6e-128">출력</span><span class="sxs-lookup"><span data-stu-id="f4c6e-128">OUTPUTS</span></span>

### <span data-ttu-id="f4c6e-129">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="f4c6e-129">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span></span>

## <span data-ttu-id="f4c6e-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f4c6e-130">NOTES</span></span>

## <span data-ttu-id="f4c6e-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f4c6e-131">RELATED LINKS</span></span>
