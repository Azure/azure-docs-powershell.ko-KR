---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 939320CB-2595-4150-AFDD-500CEA78559C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvm
schema: 2.0.0
ms.openlocfilehash: d17d01295d118c3927c127a367747cfde428ccfd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525280"
---
# <span data-ttu-id="a43f1-101">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a43f1-101">Set-AzureRmVM</span></span>

## <span data-ttu-id="a43f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a43f1-102">SYNOPSIS</span></span>
<span data-ttu-id="a43f1-103">가상 컴퓨터를 일반화 된 것으로 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a43f1-103">Marks a virtual machine as generalized.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a43f1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a43f1-104">SYNTAX</span></span>

### <span data-ttu-id="a43f1-105">GeneralizeResourceGroupNameParameterSetName (기본값)</span><span class="sxs-lookup"><span data-stu-id="a43f1-105">GeneralizeResourceGroupNameParameterSetName (Default)</span></span>
```
Set-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-Generalized] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a43f1-106">RedeployResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="a43f1-106">RedeployResourceGroupNameParameterSetName</span></span>
```
Set-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-Redeploy] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a43f1-107">GeneralizeIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="a43f1-107">GeneralizeIdParameterSetName</span></span>
```
Set-AzureRmVM [-Id] <String> [-Name] <String> [-Generalized] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a43f1-108">RedeployIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="a43f1-108">RedeployIdParameterSetName</span></span>
```
Set-AzureRmVM [-Id] <String> [-Name] <String> [-Redeploy] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a43f1-109">설명은</span><span class="sxs-lookup"><span data-stu-id="a43f1-109">DESCRIPTION</span></span>
<span data-ttu-id="a43f1-110">**AzureRmVM** cmdlet은 가상 컴퓨터를 일반화 된 것으로 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a43f1-110">The **Set-AzureRmVM** cmdlet marks a virtual machine as generalized.</span></span>
<span data-ttu-id="a43f1-111">이 cmdlet을 실행 하기 전에 가상 컴퓨터에 로그온 하 고 Sysprep를 사용 하 여 하드 디스크를 준비 합니다.</span><span class="sxs-lookup"><span data-stu-id="a43f1-111">Before you run this cmdlet, log on to the virtual machine and use Sysprep to prepare the hard disk.</span></span>

## <span data-ttu-id="a43f1-112">예제의</span><span class="sxs-lookup"><span data-stu-id="a43f1-112">EXAMPLES</span></span>

### <span data-ttu-id="a43f1-113">예제 1: 가상 컴퓨터를 일반화로 표시</span><span class="sxs-lookup"><span data-stu-id="a43f1-113">Example 1: Mark a virtual machine as generalized</span></span>
```
PS C:\> Set-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized
```

<span data-ttu-id="a43f1-114">이 명령은 VirtualMachine07 이라는 가상 컴퓨터를 일반화 된 것으로 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a43f1-114">This command marks the virtual machine named VirtualMachine07 as generalized.</span></span>

## <span data-ttu-id="a43f1-115">변수</span><span class="sxs-lookup"><span data-stu-id="a43f1-115">PARAMETERS</span></span>

### <span data-ttu-id="a43f1-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a43f1-116">-AsJob</span></span>
<span data-ttu-id="a43f1-117">백그라운드에서 cmdlet을 실행 하 고 작업을 반환 하 여 진행률을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="a43f1-117">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a43f1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a43f1-118">-DefaultProfile</span></span>
<span data-ttu-id="a43f1-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a43f1-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a43f1-120">일반화</span><span class="sxs-lookup"><span data-stu-id="a43f1-120">-Generalized</span></span>
<span data-ttu-id="a43f1-121">이 cmdlet이 가상 컴퓨터를 일반화 된 것으로 표시 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a43f1-121">Indicates that this cmdlet marks a virtual machine as generalized.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, GeneralizeIdParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a43f1-122">-Id</span><span class="sxs-lookup"><span data-stu-id="a43f1-122">-Id</span></span>
<span data-ttu-id="a43f1-123">가상 컴퓨터의 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a43f1-123">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: GeneralizeIdParameterSetName, RedeployIdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a43f1-124">-이름</span><span class="sxs-lookup"><span data-stu-id="a43f1-124">-Name</span></span>
<span data-ttu-id="a43f1-125">이 cmdlet이 작동 하는 가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a43f1-125">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a43f1-126">-재배포</span><span class="sxs-lookup"><span data-stu-id="a43f1-126">-Redeploy</span></span>
<span data-ttu-id="a43f1-127">이 cmdlet이 가상 컴퓨터를 다른 Azure 호스트에 수동으로 다시 배포 하 여 문제를 해결 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a43f1-127">Indicates that this cmdlet manually redeploys the virtual machine to a different Azure host to fix any problems.</span></span>

<span data-ttu-id="a43f1-128">가상 컴퓨터를 다시 배포 하는 경우 삭제 되 고,이로 인해 임시 드라이브 데이터가 손실 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a43f1-128">If you redeploy a virtual machine, it restarts, which results in the loss of ephemeral drive data.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RedeployResourceGroupNameParameterSetName, RedeployIdParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a43f1-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a43f1-129">-ResourceGroupName</span></span>
<span data-ttu-id="a43f1-130">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a43f1-130">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, RedeployResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a43f1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a43f1-131">CommonParameters</span></span>
<span data-ttu-id="a43f1-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a43f1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a43f1-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a43f1-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a43f1-134">입력</span><span class="sxs-lookup"><span data-stu-id="a43f1-134">INPUTS</span></span>

### <span data-ttu-id="a43f1-135">않아야</span><span class="sxs-lookup"><span data-stu-id="a43f1-135">None</span></span>
<span data-ttu-id="a43f1-136">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a43f1-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a43f1-137">출력</span><span class="sxs-lookup"><span data-stu-id="a43f1-137">OUTPUTS</span></span>

### <span data-ttu-id="a43f1-138">PSComputeLongRunningOperation를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="a43f1-138">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="a43f1-139">상속자</span><span class="sxs-lookup"><span data-stu-id="a43f1-139">NOTES</span></span>

## <span data-ttu-id="a43f1-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a43f1-140">RELATED LINKS</span></span>

[<span data-ttu-id="a43f1-141">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a43f1-141">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

