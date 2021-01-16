---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azdiskimagereference
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskImageReference.md
ms.openlocfilehash: 78a6c3bf85fae4fab9c5b9a06c366760b55804fb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98337142"
---
# <span data-ttu-id="2c605-101">Set-AzDiskImageReference</span><span class="sxs-lookup"><span data-stu-id="2c605-101">Set-AzDiskImageReference</span></span>

## <span data-ttu-id="2c605-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c605-102">SYNOPSIS</span></span>
<span data-ttu-id="2c605-103">디스크 개체에 대한 이미지 참조 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="2c605-103">Sets the image reference properties on a disk object.</span></span>

## <span data-ttu-id="2c605-104">구문</span><span class="sxs-lookup"><span data-stu-id="2c605-104">SYNTAX</span></span>

```
Set-AzDiskImageReference [-Disk] <PSDisk> [[-Id] <String>] [[-Lun] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c605-105">설명</span><span class="sxs-lookup"><span data-stu-id="2c605-105">DESCRIPTION</span></span>
<span data-ttu-id="2c605-106">**Set-AzDiskImageReference** cmdlet은 디스크 개체에 대한 이미지 참조 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="2c605-106">The **Set-AzDiskImageReference** cmdlet sets the image reference properties on a disk object.</span></span>

## <span data-ttu-id="2c605-107">예제</span><span class="sxs-lookup"><span data-stu-id="2c605-107">EXAMPLES</span></span>

### <span data-ttu-id="2c605-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="2c605-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $diskconfig = Set-AzDiskImageReference -Disk $diskconfig -Id $image -Lun 0;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="2c605-109">첫 번째 명령은 저장소 계정 유형에 따라 크기가 10GB인 Premium_LRS 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2c605-109">The first command creates a local disk object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="2c605-110">Windows OS 유형도 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="2c605-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="2c605-111">두 번째 명령은 디스크 개체에 대한 이미지 ID와 논리 단위 번호 0을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="2c605-111">The second command sets the image id and the logical unit number 0 for the disk object.</span></span>
<span data-ttu-id="2c605-112">마지막 명령은 디스크 개체를 사용하며 리소스 그룹 'ResourceGroup01'에 'Disk01'으로 디스크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2c605-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="2c605-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2c605-113">PARAMETERS</span></span>

### <span data-ttu-id="2c605-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c605-114">-DefaultProfile</span></span>
<span data-ttu-id="2c605-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2c605-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c605-116">-Disk</span><span class="sxs-lookup"><span data-stu-id="2c605-116">-Disk</span></span>
<span data-ttu-id="2c605-117">로컬 디스크 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2c605-117">Specifies a local disk object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2c605-118">-Id</span><span class="sxs-lookup"><span data-stu-id="2c605-118">-Id</span></span>
<span data-ttu-id="2c605-119">ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2c605-119">Specifies the ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c605-120">-Lun</span><span class="sxs-lookup"><span data-stu-id="2c605-120">-Lun</span></span>
<span data-ttu-id="2c605-121">LUN(논리 단위 번호)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2c605-121">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c605-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2c605-122">-Confirm</span></span>
<span data-ttu-id="2c605-123">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="2c605-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c605-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c605-124">-WhatIf</span></span>
<span data-ttu-id="2c605-125">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="2c605-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2c605-126">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2c605-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c605-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c605-127">CommonParameters</span></span>
<span data-ttu-id="2c605-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2c605-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c605-129">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2c605-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c605-130">입력</span><span class="sxs-lookup"><span data-stu-id="2c605-130">INPUTS</span></span>

### <span data-ttu-id="2c605-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="2c605-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

### <span data-ttu-id="2c605-132">System.String</span><span class="sxs-lookup"><span data-stu-id="2c605-132">System.String</span></span>

### <span data-ttu-id="2c605-133">System.Int32</span><span class="sxs-lookup"><span data-stu-id="2c605-133">System.Int32</span></span>

## <span data-ttu-id="2c605-134">출력</span><span class="sxs-lookup"><span data-stu-id="2c605-134">OUTPUTS</span></span>

### <span data-ttu-id="2c605-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="2c605-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="2c605-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2c605-136">NOTES</span></span>

## <span data-ttu-id="2c605-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2c605-137">RELATED LINKS</span></span>