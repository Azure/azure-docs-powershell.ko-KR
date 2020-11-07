---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/disable-azsecurityadvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/DIsable-AzSecurityAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/DIsable-AzSecurityAdvancedThreatProtection.md
ms.openlocfilehash: a3e83b4c58a7de2a0c020bc156e78656a6fd75ff
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699265"
---
# <span data-ttu-id="ed399-101">Disable-AzSecurityAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="ed399-101">Disable-AzSecurityAdvancedThreatProtection</span></span>

## <span data-ttu-id="ed399-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed399-102">SYNOPSIS</span></span>
<span data-ttu-id="ed399-103">저장소 계정에 대 한 고급 위협 보호 정책을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed399-103">Disables the advanced threat protection policy for a storage account.</span></span>

## <span data-ttu-id="ed399-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ed399-104">SYNTAX</span></span>

```
Disable-AzSecurityAdvancedThreatProtection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed399-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ed399-105">DESCRIPTION</span></span>
<span data-ttu-id="ed399-106">`Disable-AzSecurityAdvancedThreatProtection`Cmdlet에서 저장소 계정에 대 한 위협 protetion 정책을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed399-106">The `Disable-AzSecurityAdvancedThreatProtection` cmdlet disables the threat protetion policy for a storage account.</span></span>
<span data-ttu-id="ed399-107">이 cmdlet을 사용 하려면 *ResourceId* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed399-107">To use this cmdlet, specify the *ResourceId* parameter.</span></span>

## <span data-ttu-id="ed399-108">예제의</span><span class="sxs-lookup"><span data-stu-id="ed399-108">EXAMPLES</span></span>

### <span data-ttu-id="ed399-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="ed399-109">Example 1</span></span>
```powershell
PS C:\> Disable-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"

IsEnabled Id
--------- --
    False  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"
```

<span data-ttu-id="ed399-110">이 명령은 리소스 id에 대 한 고급 위협 보호 정책을 사용 하지 않도록 설정 합니다 `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"` .</span><span class="sxs-lookup"><span data-stu-id="ed399-110">This command disables the advanced threat protection policy for resource id `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"`.</span></span>

## <span data-ttu-id="ed399-111">변수</span><span class="sxs-lookup"><span data-stu-id="ed399-111">PARAMETERS</span></span>

### <span data-ttu-id="ed399-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed399-112">-DefaultProfile</span></span>
<span data-ttu-id="ed399-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ed399-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed399-114">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ed399-114">-ResourceId</span></span>
<span data-ttu-id="ed399-115">명령을 호출 하려는 보안 리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ed399-115">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="ed399-116">-확인</span><span class="sxs-lookup"><span data-stu-id="ed399-116">-Confirm</span></span>
<span data-ttu-id="ed399-117">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed399-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed399-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed399-118">-WhatIf</span></span>
<span data-ttu-id="ed399-119">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ed399-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ed399-120">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ed399-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed399-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed399-121">CommonParameters</span></span>
<span data-ttu-id="ed399-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed399-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed399-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed399-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed399-124">입력</span><span class="sxs-lookup"><span data-stu-id="ed399-124">INPUTS</span></span>

### <span data-ttu-id="ed399-125">않아야</span><span class="sxs-lookup"><span data-stu-id="ed399-125">None</span></span>

## <span data-ttu-id="ed399-126">출력</span><span class="sxs-lookup"><span data-stu-id="ed399-126">OUTPUTS</span></span>

### <span data-ttu-id="ed399-127">AdvancedThreatProtection. PSAdvancedThreatProtection에 대 한 Microsoft</span><span class="sxs-lookup"><span data-stu-id="ed399-127">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span></span>

## <span data-ttu-id="ed399-128">상속자</span><span class="sxs-lookup"><span data-stu-id="ed399-128">NOTES</span></span>

## <span data-ttu-id="ed399-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ed399-129">RELATED LINKS</span></span>
