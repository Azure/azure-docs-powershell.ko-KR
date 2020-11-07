---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmssvmdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVMDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVMDiskEncryption.md
ms.openlocfilehash: 50436e781304981c847b0b80dedc6fdfbc69fe1b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697406"
---
# <span data-ttu-id="f8021-101">Get-AzVmssVMDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="f8021-101">Get-AzVmssVMDiskEncryption</span></span>

## <span data-ttu-id="f8021-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8021-102">SYNOPSIS</span></span>
<span data-ttu-id="f8021-103">VM 단위 집합에서 Vm의 디스크 암호화 상태를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8021-103">Shows the disk encryption status of VMs in a VM scale set.</span></span>

## <span data-ttu-id="f8021-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f8021-104">SYNTAX</span></span>

```
Get-AzVmssVMDiskEncryption [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String>]
 [-ExtensionName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8021-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f8021-105">DESCRIPTION</span></span>
<span data-ttu-id="f8021-106">VM 확장 집합의 디스크 암호화 상태를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8021-106">Shows the disk encryption status of VM scale set.</span></span>

## <span data-ttu-id="f8021-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f8021-107">EXAMPLES</span></span>

### <span data-ttu-id="f8021-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="f8021-108">Example 1</span></span>
```
PS C:\> Get-AzVmssVMDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001" -InstanceId "1"
```

<span data-ttu-id="f8021-109">Group001 이라는 리소스 그룹에 속하는 VMSS001 이라는 VM 크기 집합에서 VM 인스턴스 1의 디스크 암호화 상태를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8021-109">Shows the disk encryption status of VM instance 1 in the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="f8021-110">변수</span><span class="sxs-lookup"><span data-stu-id="f8021-110">PARAMETERS</span></span>

### <span data-ttu-id="f8021-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8021-111">-DefaultProfile</span></span>
<span data-ttu-id="f8021-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f8021-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8021-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="f8021-113">-ExtensionName</span></span>
<span data-ttu-id="f8021-114">확장명 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f8021-114">The extension name.</span></span>
<span data-ttu-id="f8021-115">이 매개 변수를 지정 하지 않으면 windows Vm 용 azurediskencryption 용 AzureDiskEncryption를 사용 하 여 기본 값을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f8021-115">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8021-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="f8021-116">-InstanceId</span></span>
<span data-ttu-id="f8021-117">인스턴스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8021-117">Specifies the instance ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8021-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8021-118">-ResourceGroupName</span></span>
<span data-ttu-id="f8021-119">가상 컴퓨터 크기 집합의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f8021-119">Resource group name of the virtual machine scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8021-120">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="f8021-120">-VMScaleSetName</span></span>
<span data-ttu-id="f8021-121">가상 컴퓨터 크기 조정 집합 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f8021-121">The virtual machine scale set name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8021-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8021-122">CommonParameters</span></span>
<span data-ttu-id="f8021-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8021-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8021-124">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f8021-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8021-125">입력</span><span class="sxs-lookup"><span data-stu-id="f8021-125">INPUTS</span></span>

### <span data-ttu-id="f8021-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f8021-126">System.String</span></span>

## <span data-ttu-id="f8021-127">출력</span><span class="sxs-lookup"><span data-stu-id="f8021-127">OUTPUTS</span></span>

### <span data-ttu-id="f8021-128">PSVmssVMDiskEncryptionStatusContext를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8021-128">Microsoft.Azure.Commands.Compute.Models.PSVmssVMDiskEncryptionStatusContext</span></span>

## <span data-ttu-id="f8021-129">상속자</span><span class="sxs-lookup"><span data-stu-id="f8021-129">NOTES</span></span>

## <span data-ttu-id="f8021-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f8021-130">RELATED LINKS</span></span>
