---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 32CF9DA7-5607-4CF9-A2D0-D76A0C005FDA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmaccessextension
schema: 2.0.0
ms.openlocfilehash: 5d07d90e7a9902713be3ef4d2acf3a2650e4f1b4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881130"
---
# <span data-ttu-id="c22a8-101">Get-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="c22a8-101">Get-AzureRmVMAccessExtension</span></span>

## <span data-ttu-id="c22a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c22a8-102">SYNOPSIS</span></span>
<span data-ttu-id="c22a8-103">VMAccess 확장에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c22a8-103">Gets information about the VMAccess extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c22a8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c22a8-104">SYNTAX</span></span>

```
Get-AzureRmVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c22a8-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c22a8-105">DESCRIPTION</span></span>
<span data-ttu-id="c22a8-106">**AzureRmVMAccessExtension** Cmdlet은 vmaccess (Virtual machine Access) 가상 컴퓨터 확장에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c22a8-106">The **Get-AzureRmVMAccessExtension** cmdlet gets information about the Virtual Machine Access (VMAccess) Virtual Machine Extension.</span></span>

## <span data-ttu-id="c22a8-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c22a8-107">EXAMPLES</span></span>

### <span data-ttu-id="c22a8-108">예제 1: VMAccess 확장 가져오기</span><span class="sxs-lookup"><span data-stu-id="c22a8-108">Example 1: Get the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzureRmVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest"
```

<span data-ttu-id="c22a8-109">이 명령은 VirtualMachine07 이라는 가상 컴퓨터에 대 한 ContosoTest 이라는 VMAccess 확장을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c22a8-109">This command gets the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="c22a8-110">예제 2: VMAccess 확장의 인스턴스 뷰 가져오기</span><span class="sxs-lookup"><span data-stu-id="c22a8-110">Example 2: Get the instance view of the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzureRmVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest" -Status
```

<span data-ttu-id="c22a8-111">이 명령은 VirtualMachine07 이라는 가상 컴퓨터에 대해 ContosoTest 이라는 VMAccess 확장의 인스턴스 보기를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c22a8-111">This command gets the instance view of the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="c22a8-112">변수</span><span class="sxs-lookup"><span data-stu-id="c22a8-112">PARAMETERS</span></span>

### <span data-ttu-id="c22a8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c22a8-113">-DefaultProfile</span></span>
<span data-ttu-id="c22a8-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c22a8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c22a8-115">-이름</span><span class="sxs-lookup"><span data-stu-id="c22a8-115">-Name</span></span>
<span data-ttu-id="c22a8-116">이 cmdlet이 가져오는 확장의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c22a8-116">Specifies the name of the extension that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c22a8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c22a8-117">-ResourceGroupName</span></span>
<span data-ttu-id="c22a8-118">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c22a8-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="c22a8-119">-상태</span><span class="sxs-lookup"><span data-stu-id="c22a8-119">-Status</span></span>
<span data-ttu-id="c22a8-120">이 cmdlet이 확장의 인스턴스 보기만을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c22a8-120">Indicates that this cmdlet gets only the instance view of the extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c22a8-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="c22a8-121">-VMName</span></span>
<span data-ttu-id="c22a8-122">가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c22a8-122">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="c22a8-123">이 cmdlet은이 매개 변수에서 지정 하는 가상 컴퓨터에 대 한 VMAccess에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c22a8-123">This cmdlet gets information about VMAccess for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c22a8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c22a8-124">CommonParameters</span></span>
<span data-ttu-id="c22a8-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c22a8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c22a8-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c22a8-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c22a8-127">입력</span><span class="sxs-lookup"><span data-stu-id="c22a8-127">INPUTS</span></span>

### <span data-ttu-id="c22a8-128">않아야</span><span class="sxs-lookup"><span data-stu-id="c22a8-128">None</span></span>
<span data-ttu-id="c22a8-129">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c22a8-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c22a8-130">출력</span><span class="sxs-lookup"><span data-stu-id="c22a8-130">OUTPUTS</span></span>

### <span data-ttu-id="c22a8-131">VirtualMachineAccessExtensionContext를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="c22a8-131">Microsoft.Azure.Commands.Compute.Models.VirtualMachineAccessExtensionContext</span></span>

## <span data-ttu-id="c22a8-132">상속자</span><span class="sxs-lookup"><span data-stu-id="c22a8-132">NOTES</span></span>

## <span data-ttu-id="c22a8-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c22a8-133">RELATED LINKS</span></span>

[<span data-ttu-id="c22a8-134">제거-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="c22a8-134">Remove-AzureRmVMAccessExtension</span></span>](./Remove-AzureRmVMAccessExtension.md)

[<span data-ttu-id="c22a8-135">Set-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="c22a8-135">Set-AzureRmVMAccessExtension</span></span>](./Set-AzureRmVMAccessExtension.md)

[<span data-ttu-id="c22a8-136">Get-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="c22a8-136">Get-AzureRmVMExtension</span></span>](./Get-AzureRmVMExtension.md)


