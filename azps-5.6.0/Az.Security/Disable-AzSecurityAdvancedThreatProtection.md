---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/disable-azsecurityadvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Disable-AzSecurityAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Disable-AzSecurityAdvancedThreatProtection.md
ms.openlocfilehash: ed59b77a934787b1030166b24e9ed3af81698c16
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986603"
---
# <span data-ttu-id="15014-101">Disable-AzSecurityAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="15014-101">Disable-AzSecurityAdvancedThreatProtection</span></span>

## <span data-ttu-id="15014-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15014-102">SYNOPSIS</span></span>
<span data-ttu-id="15014-103">저장소/cosmosDB 계정에 대한 고급 위협 보호 정책을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="15014-103">Disables the advanced threat protection policy for a storage / cosmosDB account.</span></span>

## <span data-ttu-id="15014-104">구문</span><span class="sxs-lookup"><span data-stu-id="15014-104">SYNTAX</span></span>

```
Disable-AzSecurityAdvancedThreatProtection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15014-105">설명</span><span class="sxs-lookup"><span data-stu-id="15014-105">DESCRIPTION</span></span>
<span data-ttu-id="15014-106">`Disable-AzSecurityAdvancedThreatProtection`cmdlet은 저장소/cosmosDB 계정에 대한 위협 보호 정책을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="15014-106">The `Disable-AzSecurityAdvancedThreatProtection` cmdlet disables the threat protection policy for a storage / cosmosDB account.</span></span>
<span data-ttu-id="15014-107">이 cmdlet을 사용하 는 ResourceId 매개 *변수를* 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="15014-107">To use this cmdlet, specify the *ResourceId* parameter.</span></span>

## <span data-ttu-id="15014-108">예제</span><span class="sxs-lookup"><span data-stu-id="15014-108">EXAMPLES</span></span>

### <span data-ttu-id="15014-109">예제 1 : 저장소 계정</span><span class="sxs-lookup"><span data-stu-id="15014-109">Example 1 : Storage Account</span></span>
```powershell
PS C:\> Disable-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"

IsEnabled Id
--------- --
    False  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"
```

<span data-ttu-id="15014-110">이 명령은 리소스 ID에 대한 고급 위협 보호 정책을 사용하지 않도록 `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"` 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="15014-110">This command disables the advanced threat protection policy for resource id `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"`.</span></span>

### <span data-ttu-id="15014-111">예제 2 : CosmosDB 계정</span><span class="sxs-lookup"><span data-stu-id="15014-111">Example 2 : CosmosDB Account</span></span>
```powershell
PS C:\> Disable-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"

IsEnabled Id
--------- --
    False  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"
```

<span data-ttu-id="15014-112">이 명령은 리소스 ID에 대한 고급 위협 보호 정책을 사용하지 않도록 ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"` 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="15014-112">This command disables the advanced threat protection policy for resource id ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"`.</span></span>

## <span data-ttu-id="15014-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="15014-113">PARAMETERS</span></span>

### <span data-ttu-id="15014-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15014-114">-DefaultProfile</span></span>
<span data-ttu-id="15014-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="15014-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15014-116">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="15014-116">-ResourceId</span></span>
<span data-ttu-id="15014-117">명령을 호출할 보안 리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="15014-117">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="15014-118">-확인</span><span class="sxs-lookup"><span data-stu-id="15014-118">-Confirm</span></span>
<span data-ttu-id="15014-119">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="15014-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15014-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15014-120">-WhatIf</span></span>
<span data-ttu-id="15014-121">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="15014-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="15014-122">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="15014-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15014-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15014-123">CommonParameters</span></span>
<span data-ttu-id="15014-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="15014-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15014-125">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="15014-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15014-126">입력</span><span class="sxs-lookup"><span data-stu-id="15014-126">INPUTS</span></span>

### <span data-ttu-id="15014-127">없음</span><span class="sxs-lookup"><span data-stu-id="15014-127">None</span></span>

## <span data-ttu-id="15014-128">출력</span><span class="sxs-lookup"><span data-stu-id="15014-128">OUTPUTS</span></span>

### <span data-ttu-id="15014-129">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="15014-129">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span></span>

## <span data-ttu-id="15014-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="15014-130">NOTES</span></span>

## <span data-ttu-id="15014-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="15014-131">RELATED LINKS</span></span>
