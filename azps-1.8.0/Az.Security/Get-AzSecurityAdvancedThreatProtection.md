---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/get-azsecurityadvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdvancedThreatProtection.md
ms.openlocfilehash: 8957a794660750f45f295b77d921e647d368e7dc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699258"
---
# <span data-ttu-id="8ef60-101">Get-AzSecurityAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="8ef60-101">Get-AzSecurityAdvancedThreatProtection</span></span>

## <span data-ttu-id="8ef60-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ef60-102">SYNOPSIS</span></span>
<span data-ttu-id="8ef60-103">저장소 계정에 대 한 고급 위협 보호 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8ef60-103">Gets the advanced threat protection policy for a storage account.</span></span>

## <span data-ttu-id="8ef60-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8ef60-104">SYNTAX</span></span>

```
Get-AzSecurityAdvancedThreatProtection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8ef60-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8ef60-105">DESCRIPTION</span></span>
<span data-ttu-id="8ef60-106">`Get-AzSecurityAdvancedThreatProtection`Cmdlet은 저장소 계정에 대 한 위협 보호 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8ef60-106">The `Get-AzSecurityAdvancedThreatProtection` cmdlet gets the threat protection policy for a storage account.</span></span>
<span data-ttu-id="8ef60-107">이 cmdlet을 사용 하려면 *ResourceId* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ef60-107">To use this cmdlet, specify the *ResourceId* parameter.</span></span>

## <span data-ttu-id="8ef60-108">예제의</span><span class="sxs-lookup"><span data-stu-id="8ef60-108">EXAMPLES</span></span>

### <span data-ttu-id="8ef60-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="8ef60-109">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"

IsEnabled Id
--------- --
    False  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"
```

<span data-ttu-id="8ef60-110">이 명령은 리소스 id에 대 한 고급 위협 보호 정책을 가져옵니다 `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"` .</span><span class="sxs-lookup"><span data-stu-id="8ef60-110">This command gets the advanced threat protection policy for resource id `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"`.</span></span>

## <span data-ttu-id="8ef60-111">변수</span><span class="sxs-lookup"><span data-stu-id="8ef60-111">PARAMETERS</span></span>

### <span data-ttu-id="8ef60-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ef60-112">-DefaultProfile</span></span>
<span data-ttu-id="8ef60-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8ef60-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ef60-114">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8ef60-114">-ResourceId</span></span>
<span data-ttu-id="8ef60-115">명령을 호출 하려는 보안 리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="8ef60-115">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="8ef60-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ef60-116">CommonParameters</span></span>
<span data-ttu-id="8ef60-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ef60-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ef60-118">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ef60-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ef60-119">입력</span><span class="sxs-lookup"><span data-stu-id="8ef60-119">INPUTS</span></span>

### <span data-ttu-id="8ef60-120">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8ef60-120">System.String</span></span>

## <span data-ttu-id="8ef60-121">출력</span><span class="sxs-lookup"><span data-stu-id="8ef60-121">OUTPUTS</span></span>

### <span data-ttu-id="8ef60-122">AdvancedThreatProtection. PSAdvancedThreatProtection에 대 한 Microsoft</span><span class="sxs-lookup"><span data-stu-id="8ef60-122">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span></span>

## <span data-ttu-id="8ef60-123">상속자</span><span class="sxs-lookup"><span data-stu-id="8ef60-123">NOTES</span></span>

## <span data-ttu-id="8ef60-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8ef60-124">RELATED LINKS</span></span>
