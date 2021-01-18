---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskEncryptionSetAssociatedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskEncryptionSetAssociatedResource.md
ms.openlocfilehash: f85b1ffb181a277e750d6f6f4a67ef55ad2a75bc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98496098"
---
# <span data-ttu-id="d610c-101">Get-AzDiskEncryptionSetAssociatedResource</span><span class="sxs-lookup"><span data-stu-id="d610c-101">Get-AzDiskEncryptionSetAssociatedResource</span></span>

## <span data-ttu-id="d610c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d610c-102">SYNOPSIS</span></span>
<span data-ttu-id="d610c-103">지정된 디스크 암호화 집합과 연결된 리소스 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d610c-103">Gets the list of resources associated with the specified disk encryption set.</span></span>

## <span data-ttu-id="d610c-104">구문</span><span class="sxs-lookup"><span data-stu-id="d610c-104">SYNTAX</span></span>

```
Get-AzDiskEncryptionSetAssociatedResource [-ResourceGroupName] <String> [-DiskEncryptionSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d610c-105">설명</span><span class="sxs-lookup"><span data-stu-id="d610c-105">DESCRIPTION</span></span>
<span data-ttu-id="d610c-106">**Get-AzDiskEncryptionSetAssociatedResource** cmdlet은 지정된 디스크 암호화 집합과 연결된 리소스 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d610c-106">The **Get-AzDiskEncryptionSetAssociatedResource** cmdlet gets the list of resources associated with the specified disk encryption set.</span></span>

## <span data-ttu-id="d610c-107">예제</span><span class="sxs-lookup"><span data-stu-id="d610c-107">EXAMPLES</span></span>

### <span data-ttu-id="d610c-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="d610c-108">Example 1</span></span>
```powershell
PS C:\> Get-AzDiskEncryptionSetAssociatedResource -ResourceGroupName $RGname -DiskEncryptionSetName $diskEncryptionSetName

/subscriptions/xxxxx-xxx-xx/resourceGroups/exampleResourceGroup/providers/Microsoft.Compute/disks/exampleDisk01
/subscriptions/xxxxx-xxx-xx/resourceGroups/exampleResourceGroup/providers/Microsoft.Compute/disks/exmapleDisk02
```

<span data-ttu-id="d610c-109">cmdlet은 제공된 디스크 암호화 집합과 연결된 두 리소스 'exampleDisk01' 및 'exampleDisk02'를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="d610c-109">The cmdlet retrieves the two resources, 'exampleDisk01' and 'exampleDisk02', associated with the provided Disk Encryption Set</span></span>

## <span data-ttu-id="d610c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d610c-110">PARAMETERS</span></span>

### <span data-ttu-id="d610c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d610c-111">-DefaultProfile</span></span>
<span data-ttu-id="d610c-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d610c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d610c-113">-DiskEncryptionSetName</span><span class="sxs-lookup"><span data-stu-id="d610c-113">-DiskEncryptionSetName</span></span>
<span data-ttu-id="d610c-114">디스크 암호화 집합의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d610c-114">Name of disk encryption set.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d610c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d610c-115">-ResourceGroupName</span></span>
<span data-ttu-id="d610c-116">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d610c-116">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d610c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d610c-117">CommonParameters</span></span>
<span data-ttu-id="d610c-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d610c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d610c-119">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d610c-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d610c-120">입력</span><span class="sxs-lookup"><span data-stu-id="d610c-120">INPUTS</span></span>

### <span data-ttu-id="d610c-121">System.String</span><span class="sxs-lookup"><span data-stu-id="d610c-121">System.String</span></span>

## <span data-ttu-id="d610c-122">출력</span><span class="sxs-lookup"><span data-stu-id="d610c-122">OUTPUTS</span></span>

### <span data-ttu-id="d610c-123">System.Uri[]</span><span class="sxs-lookup"><span data-stu-id="d610c-123">System.Uri[]</span></span>

## <span data-ttu-id="d610c-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d610c-124">NOTES</span></span>

## <span data-ttu-id="d610c-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d610c-125">RELATED LINKS</span></span>
