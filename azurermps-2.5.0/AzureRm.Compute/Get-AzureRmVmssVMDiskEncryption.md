---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmssvmdiskencryption
schema: 2.0.0
ms.openlocfilehash: 41c18a3f9b1536e837ab8e127bfe00b62c74b5e1
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882693"
---
# <span data-ttu-id="44817-101">Get-AzureRmVmssVMDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="44817-101">Get-AzureRmVmssVMDiskEncryption</span></span>

## <span data-ttu-id="44817-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44817-102">SYNOPSIS</span></span>
<span data-ttu-id="44817-103">VM 단위 집합에서 Vm의 디스크 암호화 상태를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="44817-103">Shows the disk encryption status of VMs in a VM scale set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="44817-104">구문과</span><span class="sxs-lookup"><span data-stu-id="44817-104">SYNTAX</span></span>

```
Get-AzureRmVmssVMDiskEncryption [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-InstanceId] <String>] [-ExtensionName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="44817-105">설명은</span><span class="sxs-lookup"><span data-stu-id="44817-105">DESCRIPTION</span></span>
<span data-ttu-id="44817-106">VM 확장 집합의 디스크 암호화 상태를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="44817-106">Shows the disk encryption status of VM scale set.</span></span>

## <span data-ttu-id="44817-107">예제의</span><span class="sxs-lookup"><span data-stu-id="44817-107">EXAMPLES</span></span>

### <span data-ttu-id="44817-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="44817-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVmssVMDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001" -InstanceId "1"
```

<span data-ttu-id="44817-109">Group001 이라는 리소스 그룹에 속하는 VMSS001 이라는 VM 크기 집합에서 VM 인스턴스 1의 디스크 암호화 상태를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="44817-109">Shows the disk encryption status of VM instance 1 in the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="44817-110">변수</span><span class="sxs-lookup"><span data-stu-id="44817-110">PARAMETERS</span></span>

### <span data-ttu-id="44817-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44817-111">-DefaultProfile</span></span>
<span data-ttu-id="44817-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="44817-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44817-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="44817-113">-ExtensionName</span></span>
<span data-ttu-id="44817-114">확장명 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="44817-114">The extension name.</span></span>
<span data-ttu-id="44817-115">이 매개 변수를 지정 하지 않으면 windows Vm 용 azurediskencryption 용 AzureDiskEncryption를 사용 하 여 기본 값을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="44817-115">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44817-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="44817-116">-InstanceId</span></span>
<span data-ttu-id="44817-117">인스턴스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="44817-117">Specifies the instance ID.</span></span>

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

### <span data-ttu-id="44817-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44817-118">-ResourceGroupName</span></span>
<span data-ttu-id="44817-119">가상 컴퓨터 크기 집합의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="44817-119">Resource group name of the virtual machine scale set.</span></span>

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

### <span data-ttu-id="44817-120">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="44817-120">-VMScaleSetName</span></span>
<span data-ttu-id="44817-121">가상 컴퓨터 크기 조정 집합 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="44817-121">The virtual machine scale set name.</span></span>

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

### <span data-ttu-id="44817-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44817-122">CommonParameters</span></span>
<span data-ttu-id="44817-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="44817-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44817-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44817-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44817-125">입력</span><span class="sxs-lookup"><span data-stu-id="44817-125">INPUTS</span></span>

### <span data-ttu-id="44817-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="44817-126">System.String</span></span>

## <span data-ttu-id="44817-127">출력</span><span class="sxs-lookup"><span data-stu-id="44817-127">OUTPUTS</span></span>

### <span data-ttu-id="44817-128">PSVmssVMDiskEncryptionStatusContext를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="44817-128">Microsoft.Azure.Commands.Compute.Models.PSVmssVMDiskEncryptionStatusContext</span></span>

## <span data-ttu-id="44817-129">상속자</span><span class="sxs-lookup"><span data-stu-id="44817-129">NOTES</span></span>

## <span data-ttu-id="44817-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="44817-130">RELATED LINKS</span></span>

