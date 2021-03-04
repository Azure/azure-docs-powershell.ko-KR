---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskEncryptionSet.md
ms.openlocfilehash: 344bba00d610b5e23b2af5bce8476185e8bee377
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969312"
---
# <span data-ttu-id="6f894-101">Get-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="6f894-101">Get-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="6f894-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f894-102">SYNOPSIS</span></span>
<span data-ttu-id="6f894-103">디스크 암호화 집합을 얻거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="6f894-103">Get or list disk encryption sets.</span></span>

## <span data-ttu-id="6f894-104">구문</span><span class="sxs-lookup"><span data-stu-id="6f894-104">SYNTAX</span></span>

```
Get-AzDiskEncryptionSet [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f894-105">설명</span><span class="sxs-lookup"><span data-stu-id="6f894-105">DESCRIPTION</span></span>
<span data-ttu-id="6f894-106">디스크 암호화 집합을 얻거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="6f894-106">Get or list disk encryption sets.</span></span>

## <span data-ttu-id="6f894-107">예제</span><span class="sxs-lookup"><span data-stu-id="6f894-107">EXAMPLES</span></span>

### <span data-ttu-id="6f894-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="6f894-108">Example 1</span></span>
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

<span data-ttu-id="6f894-109">'enc1' 디스크 암호화 집합을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6f894-109">Get disk encryption set 'enc1'</span></span>

### <span data-ttu-id="6f894-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="6f894-110">Example 2</span></span>
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

<span data-ttu-id="6f894-111">리소스 그룹 'rg1'에서 모든 디스크 암호화 집합을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6f894-111">Get all disk encryption sets in resource group 'rg1'.</span></span>

### <span data-ttu-id="6f894-112">예제 3</span><span class="sxs-lookup"><span data-stu-id="6f894-112">Example 3</span></span>
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

<span data-ttu-id="6f894-113">구독에서 모든 디스크 암호화 집합을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6f894-113">Get all disk encryption sets in subscription.</span></span>

## <span data-ttu-id="6f894-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="6f894-114">PARAMETERS</span></span>

### <span data-ttu-id="6f894-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f894-115">-DefaultProfile</span></span>
<span data-ttu-id="6f894-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6f894-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f894-117">-Name</span><span class="sxs-lookup"><span data-stu-id="6f894-117">-Name</span></span>
<span data-ttu-id="6f894-118">디스크 암호화 집합의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6f894-118">Name of disk encryption set.</span></span>

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

### <span data-ttu-id="6f894-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f894-119">-ResourceGroupName</span></span>
<span data-ttu-id="6f894-120">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6f894-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="6f894-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f894-121">CommonParameters</span></span>
<span data-ttu-id="6f894-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6f894-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f894-123">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6f894-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f894-124">입력</span><span class="sxs-lookup"><span data-stu-id="6f894-124">INPUTS</span></span>

### <span data-ttu-id="6f894-125">System.String</span><span class="sxs-lookup"><span data-stu-id="6f894-125">System.String</span></span>

## <span data-ttu-id="6f894-126">출력</span><span class="sxs-lookup"><span data-stu-id="6f894-126">OUTPUTS</span></span>

### <span data-ttu-id="6f894-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="6f894-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="6f894-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6f894-128">NOTES</span></span>

## <span data-ttu-id="6f894-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6f894-129">RELATED LINKS</span></span>
