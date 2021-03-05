---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azsnapshotimagereference
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotImageReference.md
ms.openlocfilehash: 6746bc96f7c1a14d617f3147676556be7402b71c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008016"
---
# <span data-ttu-id="aa20c-101">Set-AzSnapshotImageReference</span><span class="sxs-lookup"><span data-stu-id="aa20c-101">Set-AzSnapshotImageReference</span></span>

## <span data-ttu-id="aa20c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa20c-102">SYNOPSIS</span></span>
<span data-ttu-id="aa20c-103">스냅숏 개체에서 이미지 참조 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="aa20c-103">Sets the image reference properties on a snapshot object.</span></span>

## <span data-ttu-id="aa20c-104">구문</span><span class="sxs-lookup"><span data-stu-id="aa20c-104">SYNTAX</span></span>

```
Set-AzSnapshotImageReference [-Snapshot] <PSSnapshot> [[-Id] <String>] [[-Lun] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa20c-105">설명</span><span class="sxs-lookup"><span data-stu-id="aa20c-105">DESCRIPTION</span></span>
<span data-ttu-id="aa20c-106">**Set-AzSnapshotImageReference** cmdlet은 스냅숏 개체의 이미지 참조 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="aa20c-106">The **Set-AzSnapshotImageReference** cmdlet sets the image reference properties on a snapshot object.</span></span>

## <span data-ttu-id="aa20c-107">예제</span><span class="sxs-lookup"><span data-stu-id="aa20c-107">EXAMPLES</span></span>

### <span data-ttu-id="aa20c-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="aa20c-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzSnapshotConfig -SnapshotSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $snapshotconfig = Set-AzSnapshotImageReference -Snapshot $snapshotconfig -Id $image -Lun 0;
PS C:\> New-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="aa20c-109">첫 번째 명령은 저장소 계정 유형에 크기가 10GB인 로컬 Premium_LRS 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="aa20c-109">The first command creates a local snapshot object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="aa20c-110">또한 Windows OS 유형을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="aa20c-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="aa20c-111">두 번째 명령은 스냅숏 개체에 대한 이미지 ID 및 논리 단위 번호 0을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="aa20c-111">The second command sets the image ID and the logical unit number 0 for the snapshot object.</span></span>
<span data-ttu-id="aa20c-112">마지막 명령은 스냅숏 개체를 만들고 리소스 그룹 'ResourceGroup01'에서 '스냅숏01'을 사용하여 스냅숏을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="aa20c-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="aa20c-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="aa20c-113">PARAMETERS</span></span>

### <span data-ttu-id="aa20c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa20c-114">-DefaultProfile</span></span>
<span data-ttu-id="aa20c-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="aa20c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aa20c-116">-Id</span><span class="sxs-lookup"><span data-stu-id="aa20c-116">-Id</span></span>
<span data-ttu-id="aa20c-117">ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="aa20c-117">Specifies the ID.</span></span>

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

### <span data-ttu-id="aa20c-118">-Lun</span><span class="sxs-lookup"><span data-stu-id="aa20c-118">-Lun</span></span>
<span data-ttu-id="aa20c-119">LUN(논리 단위 번호)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="aa20c-119">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="aa20c-120">-스냅숏</span><span class="sxs-lookup"><span data-stu-id="aa20c-120">-Snapshot</span></span>
<span data-ttu-id="aa20c-121">로컬 스냅숏 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="aa20c-121">Specifies a local snapshot object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aa20c-122">-확인</span><span class="sxs-lookup"><span data-stu-id="aa20c-122">-Confirm</span></span>
<span data-ttu-id="aa20c-123">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="aa20c-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa20c-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa20c-124">-WhatIf</span></span>
<span data-ttu-id="aa20c-125">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="aa20c-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aa20c-126">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aa20c-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa20c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa20c-127">CommonParameters</span></span>
<span data-ttu-id="aa20c-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="aa20c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa20c-129">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aa20c-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa20c-130">입력</span><span class="sxs-lookup"><span data-stu-id="aa20c-130">INPUTS</span></span>

### <span data-ttu-id="aa20c-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="aa20c-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

### <span data-ttu-id="aa20c-132">System.String</span><span class="sxs-lookup"><span data-stu-id="aa20c-132">System.String</span></span>

### <span data-ttu-id="aa20c-133">System.Int32</span><span class="sxs-lookup"><span data-stu-id="aa20c-133">System.Int32</span></span>

## <span data-ttu-id="aa20c-134">출력</span><span class="sxs-lookup"><span data-stu-id="aa20c-134">OUTPUTS</span></span>

### <span data-ttu-id="aa20c-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="aa20c-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="aa20c-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="aa20c-136">NOTES</span></span>

## <span data-ttu-id="aa20c-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aa20c-137">RELATED LINKS</span></span>
