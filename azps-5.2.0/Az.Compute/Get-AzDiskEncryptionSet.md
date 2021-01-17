---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskEncryptionSet.md
ms.openlocfilehash: 7d2b23c08f7ce910daf87f7cebbea844d5bda6f0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98332798"
---
# <span data-ttu-id="5a9dc-101">Get-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="5a9dc-101">Get-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="5a9dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a9dc-102">SYNOPSIS</span></span>
<span data-ttu-id="5a9dc-103">디스크 암호화 집합을 얻거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="5a9dc-103">Get or list disk encryption sets.</span></span>

## <span data-ttu-id="5a9dc-104">구문</span><span class="sxs-lookup"><span data-stu-id="5a9dc-104">SYNTAX</span></span>

```
Get-AzDiskEncryptionSet [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a9dc-105">설명</span><span class="sxs-lookup"><span data-stu-id="5a9dc-105">DESCRIPTION</span></span>
<span data-ttu-id="5a9dc-106">디스크 암호화 집합을 얻거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="5a9dc-106">Get or list disk encryption sets.</span></span>

## <span data-ttu-id="5a9dc-107">예제</span><span class="sxs-lookup"><span data-stu-id="5a9dc-107">EXAMPLES</span></span>

### <span data-ttu-id="5a9dc-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="5a9dc-108">Example 1</span></span>
```powershell
PS C:\> Get-AzDiskEncryptionSet -ResourceGroupName rg1 -Name enc1;

ResourceGroupName : rg1
Identity          : Microsoft.Azure.Management.Compute.Models.EncryptionSetIdentity
ActiveKey         : Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
PreviousKeys      : {}
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/diskEncryptionSets/enc1
Name              : enc1
Type              : Microsoft.Compute/diskEncryptionSets
Location          : westcentralus
Tags              : {}
```

<span data-ttu-id="5a9dc-109">디스크 암호화 집합 'enc1'을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5a9dc-109">Get disk encryption set 'enc1'</span></span>

### <span data-ttu-id="5a9dc-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="5a9dc-110">Example 2</span></span>
```powershell
PS C:\> Get-AzDiskEncryptionSet

ResourceGroupName : rg1
Identity          : Microsoft.Azure.Management.Compute.Models.EncryptionSetIdentity
ActiveKey         : Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
PreviousKeys      : {}
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/diskEncryptionSets/enc1
Name              : enc1
Type              : Microsoft.Compute/diskEncryptionSets
Location          : westcentralus
Tags              : {}

ResourceGroupName : rg1
Identity          : Microsoft.Azure.Management.Compute.Models.EncryptionSetIdentity
ActiveKey         : Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
PreviousKeys      : {}
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/diskEncryptionSets/enc2
Name              : enc2
Type              : Microsoft.Compute/diskEncryptionSets
Location          : westcentralus
Tags              : {}
```

<span data-ttu-id="5a9dc-111">리소스 그룹 'rg1'의 모든 디스크 암호화 집합을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5a9dc-111">Get all disk encryption sets in resource group 'rg1'.</span></span>

### <span data-ttu-id="5a9dc-112">예제 3</span><span class="sxs-lookup"><span data-stu-id="5a9dc-112">Example 3</span></span>
```powershell
PS C:\> Get-AzDiskEncryptionSet -ResourceGroupName rg1

ResourceGroupName : rg1
Identity          : Microsoft.Azure.Management.Compute.Models.EncryptionSetIdentity
ActiveKey         : Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
PreviousKeys      : {}
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/diskEncryptionSets/enc1
Name              : enc1
Type              : Microsoft.Compute/diskEncryptionSets
Location          : westcentralus
Tags              : {}

ResourceGroupName : rg1
Identity          : Microsoft.Azure.Management.Compute.Models.EncryptionSetIdentity
ActiveKey         : Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
PreviousKeys      : {}
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/diskEncryptionSets/enc2
Name              : enc2
Type              : Microsoft.Compute/diskEncryptionSets
Location          : westcentralus
Tags              : {}

ResourceGroupName : rg2
Identity          : Microsoft.Azure.Management.Compute.Models.EncryptionSetIdentity
ActiveKey         : Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
PreviousKeys      : {}
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/diskEncryptionSets/enc3
Name              : enc3
Type              : Microsoft.Compute/diskEncryptionSets
Location          : westcentralus
Tags              : {}
```

<span data-ttu-id="5a9dc-113">구독의 모든 디스크 암호화 집합을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5a9dc-113">Get all disk encryption sets in subscription.</span></span>

## <span data-ttu-id="5a9dc-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5a9dc-114">PARAMETERS</span></span>

### <span data-ttu-id="5a9dc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a9dc-115">-DefaultProfile</span></span>
<span data-ttu-id="5a9dc-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5a9dc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a9dc-117">-Name</span><span class="sxs-lookup"><span data-stu-id="5a9dc-117">-Name</span></span>
<span data-ttu-id="5a9dc-118">디스크 암호화 집합의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5a9dc-118">Name of disk encryption set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DiskEncryptionSetName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a9dc-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a9dc-119">-ResourceGroupName</span></span>
<span data-ttu-id="5a9dc-120">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5a9dc-120">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a9dc-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a9dc-121">CommonParameters</span></span>
<span data-ttu-id="5a9dc-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5a9dc-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a9dc-123">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5a9dc-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a9dc-124">입력</span><span class="sxs-lookup"><span data-stu-id="5a9dc-124">INPUTS</span></span>

### <span data-ttu-id="5a9dc-125">System.String</span><span class="sxs-lookup"><span data-stu-id="5a9dc-125">System.String</span></span>

## <span data-ttu-id="5a9dc-126">출력</span><span class="sxs-lookup"><span data-stu-id="5a9dc-126">OUTPUTS</span></span>

### <span data-ttu-id="5a9dc-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="5a9dc-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="5a9dc-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5a9dc-128">NOTES</span></span>

## <span data-ttu-id="5a9dc-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5a9dc-129">RELATED LINKS</span></span>
