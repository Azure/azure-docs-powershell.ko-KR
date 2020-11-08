---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmssdiskencryption
schema: 2.0.0
ms.openlocfilehash: c49fc472c6cc3693145487bdfe7488d0eabfe237
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881605"
---
# <span data-ttu-id="95309-101">Get-AzureRmVmssDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="95309-101">Get-AzureRmVmssDiskEncryption</span></span>

## <span data-ttu-id="95309-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95309-102">SYNOPSIS</span></span>
<span data-ttu-id="95309-103">VM 크기 집합의 디스크 암호화 상태를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="95309-103">Shows the disk encryption status of a VM scale set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95309-104">구문과</span><span class="sxs-lookup"><span data-stu-id="95309-104">SYNTAX</span></span>

```
Get-AzureRmVmssDiskEncryption [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [[-ExtensionName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95309-105">설명은</span><span class="sxs-lookup"><span data-stu-id="95309-105">DESCRIPTION</span></span>
<span data-ttu-id="95309-106">VM 크기 집합의 디스크 암호화 상태를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="95309-106">Shows the disk encryption status of a VM scale set.</span></span>

## <span data-ttu-id="95309-107">예제의</span><span class="sxs-lookup"><span data-stu-id="95309-107">EXAMPLES</span></span>

### <span data-ttu-id="95309-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="95309-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVmssDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="95309-109">Group001 이라는 리소스 그룹에 속하는 VMSS001 이라는 VM 소수 자릿수가 집합의 디스크 암호화 상태를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="95309-109">Shows the disk encryption status of the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="95309-110">변수</span><span class="sxs-lookup"><span data-stu-id="95309-110">PARAMETERS</span></span>

### <span data-ttu-id="95309-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95309-111">-DefaultProfile</span></span>
<span data-ttu-id="95309-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="95309-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95309-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="95309-113">-ExtensionName</span></span>
<span data-ttu-id="95309-114">확장명 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="95309-114">The extension name.</span></span>
<span data-ttu-id="95309-115">이 매개 변수를 지정 하지 않으면 windows Vm 용 azurediskencryption 용 AzureDiskEncryption를 사용 하 여 기본 값을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95309-115">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95309-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95309-116">-ResourceGroupName</span></span>
<span data-ttu-id="95309-117">가상 머신 크기 집합의 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="95309-117">Resource group name of the virtual machine scale set</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95309-118">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="95309-118">-VMScaleSetName</span></span>
<span data-ttu-id="95309-119">가상 컴퓨터 크기 조정 집합 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="95309-119">The virtual machine scale set name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95309-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95309-120">CommonParameters</span></span>
<span data-ttu-id="95309-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="95309-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95309-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95309-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95309-123">입력</span><span class="sxs-lookup"><span data-stu-id="95309-123">INPUTS</span></span>

### <span data-ttu-id="95309-124">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="95309-124">System.String</span></span>

## <span data-ttu-id="95309-125">출력</span><span class="sxs-lookup"><span data-stu-id="95309-125">OUTPUTS</span></span>

### <span data-ttu-id="95309-126">PSVmssDiskEncryptionStatusContext를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="95309-126">Microsoft.Azure.Commands.Compute.Models.PSVmssDiskEncryptionStatusContext</span></span>

## <span data-ttu-id="95309-127">상속자</span><span class="sxs-lookup"><span data-stu-id="95309-127">NOTES</span></span>

## <span data-ttu-id="95309-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="95309-128">RELATED LINKS</span></span>
