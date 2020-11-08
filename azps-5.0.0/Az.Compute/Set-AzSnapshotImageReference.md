---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azsnapshotimagereference
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotImageReference.md
ms.openlocfilehash: deb122735b94ed8ac0de63330a9fbdb3ecac81d4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217497"
---
# <span data-ttu-id="ddfc1-101">Set-AzSnapshotImageReference</span><span class="sxs-lookup"><span data-stu-id="ddfc1-101">Set-AzSnapshotImageReference</span></span>

## <span data-ttu-id="ddfc1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ddfc1-102">SYNOPSIS</span></span>
<span data-ttu-id="ddfc1-103">Snapshot 개체에 대 한 이미지 참조 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ddfc1-103">Sets the image reference properties on a snapshot object.</span></span>

## <span data-ttu-id="ddfc1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ddfc1-104">SYNTAX</span></span>

```
Set-AzSnapshotImageReference [-Snapshot] <PSSnapshot> [[-Id] <String>] [[-Lun] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ddfc1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ddfc1-105">DESCRIPTION</span></span>
<span data-ttu-id="ddfc1-106">**Set-AzSnapshotImageReference** cmdlet은 snapshot 개체의 이미지 참조 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ddfc1-106">The **Set-AzSnapshotImageReference** cmdlet sets the image reference properties on a snapshot object.</span></span>

## <span data-ttu-id="ddfc1-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ddfc1-107">EXAMPLES</span></span>

### <span data-ttu-id="ddfc1-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="ddfc1-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzSnapshotConfig -SnapshotSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $snapshotconfig = Set-AzSnapshotImageReference -Snapshot $snapshotconfig -Id $image -Lun 0;
PS C:\> New-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="ddfc1-109">첫 번째 명령은 Premium_LRS 저장소 계정 유형에 서 크기가 10GB 인 로컬 스냅숏 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ddfc1-109">The first command creates a local snapshot object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="ddfc1-110">Windows OS 종류도 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ddfc1-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="ddfc1-111">두 번째 명령은 snapshot 개체에 대 한 이미지 ID와 논리 단위 번호 0을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ddfc1-111">The second command sets the image ID and the logical unit number 0 for the snapshot object.</span></span>
<span data-ttu-id="ddfc1-112">마지막 명령은 snapshot 개체를 사용 하 여 리소스 그룹 ' ResourceGroup01 '에 이름이 ' Snapshot01 ' 인 스냅숏을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ddfc1-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="ddfc1-113">변수</span><span class="sxs-lookup"><span data-stu-id="ddfc1-113">PARAMETERS</span></span>

### <span data-ttu-id="ddfc1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddfc1-114">-DefaultProfile</span></span>
<span data-ttu-id="ddfc1-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ddfc1-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ddfc1-116">-Id</span><span class="sxs-lookup"><span data-stu-id="ddfc1-116">-Id</span></span>
<span data-ttu-id="ddfc1-117">ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ddfc1-117">Specifies the ID.</span></span>

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

### <span data-ttu-id="ddfc1-118">-Lun</span><span class="sxs-lookup"><span data-stu-id="ddfc1-118">-Lun</span></span>
<span data-ttu-id="ddfc1-119">LUN (논리 단위 번호)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ddfc1-119">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="ddfc1-120">-스냅숏</span><span class="sxs-lookup"><span data-stu-id="ddfc1-120">-Snapshot</span></span>
<span data-ttu-id="ddfc1-121">로컬 스냅숏 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ddfc1-121">Specifies a local snapshot object.</span></span>

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

### <span data-ttu-id="ddfc1-122">-확인</span><span class="sxs-lookup"><span data-stu-id="ddfc1-122">-Confirm</span></span>
<span data-ttu-id="ddfc1-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ddfc1-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddfc1-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddfc1-124">-WhatIf</span></span>
<span data-ttu-id="ddfc1-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ddfc1-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ddfc1-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ddfc1-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ddfc1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddfc1-127">CommonParameters</span></span>
<span data-ttu-id="ddfc1-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ddfc1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddfc1-129">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ddfc1-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddfc1-130">입력</span><span class="sxs-lookup"><span data-stu-id="ddfc1-130">INPUTS</span></span>

### <span data-ttu-id="ddfc1-131">Microsoft. a. a. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="ddfc1-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

### <span data-ttu-id="ddfc1-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ddfc1-132">System.String</span></span>

### <span data-ttu-id="ddfc1-133">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="ddfc1-133">System.Int32</span></span>

## <span data-ttu-id="ddfc1-134">출력</span><span class="sxs-lookup"><span data-stu-id="ddfc1-134">OUTPUTS</span></span>

### <span data-ttu-id="ddfc1-135">Microsoft. a. a. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="ddfc1-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="ddfc1-136">상속자</span><span class="sxs-lookup"><span data-stu-id="ddfc1-136">NOTES</span></span>

## <span data-ttu-id="ddfc1-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ddfc1-137">RELATED LINKS</span></span>
