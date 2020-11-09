---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskEncryptionSet.md
ms.openlocfilehash: 7d2b23c08f7ce910daf87f7cebbea844d5bda6f0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94310388"
---
# <span data-ttu-id="5c70a-101">Get-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="5c70a-101">Get-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="5c70a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c70a-102">SYNOPSIS</span></span>
<span data-ttu-id="5c70a-103">디스크 암호화 집합을 가져오거나 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c70a-103">Get or list disk encryption sets.</span></span>

## <span data-ttu-id="5c70a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5c70a-104">SYNTAX</span></span>

```
Get-AzDiskEncryptionSet [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5c70a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5c70a-105">DESCRIPTION</span></span>
<span data-ttu-id="5c70a-106">디스크 암호화 집합을 가져오거나 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c70a-106">Get or list disk encryption sets.</span></span>

## <span data-ttu-id="5c70a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="5c70a-107">EXAMPLES</span></span>

### <span data-ttu-id="5c70a-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="5c70a-108">Example 1</span></span>
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

<span data-ttu-id="5c70a-109">' Enc1 ' 디스크 암호화 집합 가져오기</span><span class="sxs-lookup"><span data-stu-id="5c70a-109">Get disk encryption set 'enc1'</span></span>

### <span data-ttu-id="5c70a-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="5c70a-110">Example 2</span></span>
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

<span data-ttu-id="5c70a-111">' Rg1 ' 리소스 그룹에서 모든 디스크 암호화 집합을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5c70a-111">Get all disk encryption sets in resource group 'rg1'.</span></span>

### <span data-ttu-id="5c70a-112">예제 3</span><span class="sxs-lookup"><span data-stu-id="5c70a-112">Example 3</span></span>
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

<span data-ttu-id="5c70a-113">구독에서 모든 디스크 암호화 집합을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5c70a-113">Get all disk encryption sets in subscription.</span></span>

## <span data-ttu-id="5c70a-114">변수</span><span class="sxs-lookup"><span data-stu-id="5c70a-114">PARAMETERS</span></span>

### <span data-ttu-id="5c70a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c70a-115">-DefaultProfile</span></span>
<span data-ttu-id="5c70a-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5c70a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c70a-117">-이름</span><span class="sxs-lookup"><span data-stu-id="5c70a-117">-Name</span></span>
<span data-ttu-id="5c70a-118">디스크 암호화 집합의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5c70a-118">Name of disk encryption set.</span></span>

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

### <span data-ttu-id="5c70a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c70a-119">-ResourceGroupName</span></span>
<span data-ttu-id="5c70a-120">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c70a-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="5c70a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c70a-121">CommonParameters</span></span>
<span data-ttu-id="5c70a-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c70a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c70a-123">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5c70a-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c70a-124">입력</span><span class="sxs-lookup"><span data-stu-id="5c70a-124">INPUTS</span></span>

### <span data-ttu-id="5c70a-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5c70a-125">System.String</span></span>

## <span data-ttu-id="5c70a-126">출력</span><span class="sxs-lookup"><span data-stu-id="5c70a-126">OUTPUTS</span></span>

### <span data-ttu-id="5c70a-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSDIska Set</span><span class="sxs-lookup"><span data-stu-id="5c70a-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="5c70a-128">상속자</span><span class="sxs-lookup"><span data-stu-id="5c70a-128">NOTES</span></span>

## <span data-ttu-id="5c70a-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5c70a-129">RELATED LINKS</span></span>
