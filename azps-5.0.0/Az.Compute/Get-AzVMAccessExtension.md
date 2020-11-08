---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 32CF9DA7-5607-4CF9-A2D0-D76A0C005FDA
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMAccessExtension.md
ms.openlocfilehash: c139e1bac6f910a1759e4482abdd7c67d2e7fa55
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215623"
---
# <span data-ttu-id="4a260-101">Get-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="4a260-101">Get-AzVMAccessExtension</span></span>

## <span data-ttu-id="4a260-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a260-102">SYNOPSIS</span></span>
<span data-ttu-id="4a260-103">VMAccess 확장에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4a260-103">Gets information about the VMAccess extension.</span></span>

## <span data-ttu-id="4a260-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4a260-104">SYNTAX</span></span>

```
Get-AzVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a260-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4a260-105">DESCRIPTION</span></span>
<span data-ttu-id="4a260-106">**AzVMAccessExtension** Cmdlet은 vmaccess (Virtual machine Access) 가상 컴퓨터 확장에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4a260-106">The **Get-AzVMAccessExtension** cmdlet gets information about the Virtual Machine Access (VMAccess) Virtual Machine Extension.</span></span>

## <span data-ttu-id="4a260-107">예제의</span><span class="sxs-lookup"><span data-stu-id="4a260-107">EXAMPLES</span></span>

### <span data-ttu-id="4a260-108">예제 1: VMAccess 확장 가져오기</span><span class="sxs-lookup"><span data-stu-id="4a260-108">Example 1: Get the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest"
```

<span data-ttu-id="4a260-109">이 명령은 VirtualMachine07 이라는 가상 컴퓨터에 대 한 ContosoTest 이라는 VMAccess 확장을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4a260-109">This command gets the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="4a260-110">예제 2: VMAccess 확장의 인스턴스 뷰 가져오기</span><span class="sxs-lookup"><span data-stu-id="4a260-110">Example 2: Get the instance view of the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest" -Status
```

<span data-ttu-id="4a260-111">이 명령은 VirtualMachine07 이라는 가상 컴퓨터에 대해 ContosoTest 이라는 VMAccess 확장의 인스턴스 보기를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4a260-111">This command gets the instance view of the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="4a260-112">변수</span><span class="sxs-lookup"><span data-stu-id="4a260-112">PARAMETERS</span></span>

### <span data-ttu-id="4a260-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a260-113">-DefaultProfile</span></span>
<span data-ttu-id="4a260-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4a260-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4a260-115">-이름</span><span class="sxs-lookup"><span data-stu-id="4a260-115">-Name</span></span>
<span data-ttu-id="4a260-116">이 cmdlet이 가져오는 확장의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a260-116">Specifies the name of the extension that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a260-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a260-117">-ResourceGroupName</span></span>
<span data-ttu-id="4a260-118">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a260-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="4a260-119">-상태</span><span class="sxs-lookup"><span data-stu-id="4a260-119">-Status</span></span>
<span data-ttu-id="4a260-120">이 cmdlet이 확장의 인스턴스 보기만을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4a260-120">Indicates that this cmdlet gets only the instance view of the extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a260-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="4a260-121">-VMName</span></span>
<span data-ttu-id="4a260-122">가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a260-122">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="4a260-123">이 cmdlet은이 매개 변수에서 지정 하는 가상 컴퓨터에 대 한 VMAccess에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4a260-123">This cmdlet gets information about VMAccess for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a260-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a260-124">CommonParameters</span></span>
<span data-ttu-id="4a260-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a260-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a260-126">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4a260-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a260-127">입력</span><span class="sxs-lookup"><span data-stu-id="4a260-127">INPUTS</span></span>

### <span data-ttu-id="4a260-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4a260-128">System.String</span></span>

### <span data-ttu-id="4a260-129">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="4a260-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4a260-130">출력</span><span class="sxs-lookup"><span data-stu-id="4a260-130">OUTPUTS</span></span>

### <span data-ttu-id="4a260-131">VirtualMachineAccessExtensionContext를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="4a260-131">Microsoft.Azure.Commands.Compute.Models.VirtualMachineAccessExtensionContext</span></span>

## <span data-ttu-id="4a260-132">상속자</span><span class="sxs-lookup"><span data-stu-id="4a260-132">NOTES</span></span>

## <span data-ttu-id="4a260-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4a260-133">RELATED LINKS</span></span>

[<span data-ttu-id="4a260-134">제거-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="4a260-134">Remove-AzVMAccessExtension</span></span>](./Remove-AzVMAccessExtension.md)

[<span data-ttu-id="4a260-135">Set-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="4a260-135">Set-AzVMAccessExtension</span></span>](./Set-AzVMAccessExtension.md)

[<span data-ttu-id="4a260-136">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="4a260-136">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)


