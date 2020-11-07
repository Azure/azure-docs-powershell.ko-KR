---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmsecret
schema: 2.0.0
ms.openlocfilehash: 8d3c10be9d4a3f165932271838f6af8fdbf18e4d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881969"
---
# <span data-ttu-id="25138-101">Remove-AzureRmVMSecret</span><span class="sxs-lookup"><span data-stu-id="25138-101">Remove-AzureRmVMSecret</span></span>

## <span data-ttu-id="25138-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25138-102">SYNOPSIS</span></span>
<span data-ttu-id="25138-103">가상 머신 개체에서 (a) 비밀을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="25138-103">Removes (a) secret(s) from a virtual machine object</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25138-104">구문과</span><span class="sxs-lookup"><span data-stu-id="25138-104">SYNTAX</span></span>

```
Remove-AzureRmVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25138-105">설명은</span><span class="sxs-lookup"><span data-stu-id="25138-105">DESCRIPTION</span></span>
<span data-ttu-id="25138-106">Remove-AzureRmVMSecret cmdlet은 가상 컴퓨터 개체에서 (a) 비밀을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="25138-106">The Remove-AzureRmVMSecret cmdlet removes (a) secret(s) from a virtual machine object.</span></span>

## <span data-ttu-id="25138-107">예제의</span><span class="sxs-lookup"><span data-stu-id="25138-107">EXAMPLES</span></span>

### <span data-ttu-id="25138-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="25138-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "rg1" -Name "vm1" | Remove-AzureRmVMSecret | Update-AzureRmVM
```

<span data-ttu-id="25138-109">리소스 그룹 "rg1"의 가상 머신 "vm1"에서 모든 비밀을 제거 하 고 VM을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="25138-109">Removes all secrets from a virtual machine "vm1" in resource group "rg1" and update the VM</span></span>

## <span data-ttu-id="25138-110">변수</span><span class="sxs-lookup"><span data-stu-id="25138-110">PARAMETERS</span></span>

### <span data-ttu-id="25138-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25138-111">-DefaultProfile</span></span>
<span data-ttu-id="25138-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="25138-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25138-113">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="25138-113">-SourceVaultId</span></span>
<span data-ttu-id="25138-114">이 cmdlet이 제거 하는 원본 보관소 Id의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="25138-114">Specifies an array of source vault IDs that this cmdlet removes.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Id

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25138-115">-VM</span><span class="sxs-lookup"><span data-stu-id="25138-115">-VM</span></span>
<span data-ttu-id="25138-116">이 cmdlet가 암호 (a)를 제거 하는 가상 컴퓨터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="25138-116">Specifies the virtual machine from which this cmdlet removes (a) secret(s).</span></span>
<span data-ttu-id="25138-117">가상 컴퓨터 개체를 가져오려면 Get-AzureRmVM cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="25138-117">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="25138-118">-확인</span><span class="sxs-lookup"><span data-stu-id="25138-118">-Confirm</span></span>
<span data-ttu-id="25138-119">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="25138-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25138-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25138-120">-WhatIf</span></span>
<span data-ttu-id="25138-121">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="25138-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25138-122">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="25138-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25138-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25138-123">CommonParameters</span></span>
<span data-ttu-id="25138-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="25138-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25138-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25138-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25138-126">입력</span><span class="sxs-lookup"><span data-stu-id="25138-126">INPUTS</span></span>

### <span data-ttu-id="25138-127">PSVirtualMachine를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="25138-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="25138-128">출력</span><span class="sxs-lookup"><span data-stu-id="25138-128">OUTPUTS</span></span>

### <span data-ttu-id="25138-129">PSVirtualMachine를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="25138-129">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="25138-130">상속자</span><span class="sxs-lookup"><span data-stu-id="25138-130">NOTES</span></span>

## <span data-ttu-id="25138-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="25138-131">RELATED LINKS</span></span>

