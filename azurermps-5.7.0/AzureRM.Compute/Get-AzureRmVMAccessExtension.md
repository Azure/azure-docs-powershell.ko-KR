---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 32CF9DA7-5607-4CF9-A2D0-D76A0C005FDA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMAccessExtension.md
ms.openlocfilehash: 9e7cb85bf29d6982271768af6948db1d3c5b8605
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529022"
---
# <span data-ttu-id="5b41f-101">Get-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="5b41f-101">Get-AzureRmVMAccessExtension</span></span>

## <span data-ttu-id="5b41f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b41f-102">SYNOPSIS</span></span>
<span data-ttu-id="5b41f-103">VMAccess 확장에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5b41f-103">Gets information about the VMAccess extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5b41f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5b41f-104">SYNTAX</span></span>

```
Get-AzureRmVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [<CommonParameters>]
```

## <span data-ttu-id="5b41f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5b41f-105">DESCRIPTION</span></span>
<span data-ttu-id="5b41f-106">**AzureRmVMAccessExtension** Cmdlet은 vmaccess (Virtual machine Access) 가상 컴퓨터 확장에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5b41f-106">The **Get-AzureRmVMAccessExtension** cmdlet gets information about the Virtual Machine Access (VMAccess) Virtual Machine Extension.</span></span>

## <span data-ttu-id="5b41f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="5b41f-107">EXAMPLES</span></span>

### <span data-ttu-id="5b41f-108">예제 1: VMAccess 확장 가져오기</span><span class="sxs-lookup"><span data-stu-id="5b41f-108">Example 1: Get the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzureRmVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest"
```

<span data-ttu-id="5b41f-109">이 명령은 VirtualMachine07 이라는 가상 컴퓨터에 대 한 ContosoTest 이라는 VMAccess 확장을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5b41f-109">This command gets the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="5b41f-110">예제 2: VMAccess 확장의 인스턴스 뷰 가져오기</span><span class="sxs-lookup"><span data-stu-id="5b41f-110">Example 2: Get the instance view of the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzureRmVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest" -Status
```

<span data-ttu-id="5b41f-111">이 명령은 VirtualMachine07 이라는 가상 컴퓨터에 대해 ContosoTest 이라는 VMAccess 확장의 인스턴스 보기를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5b41f-111">This command gets the instance view of the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="5b41f-112">변수</span><span class="sxs-lookup"><span data-stu-id="5b41f-112">PARAMETERS</span></span>

### <span data-ttu-id="5b41f-113">-이름</span><span class="sxs-lookup"><span data-stu-id="5b41f-113">-Name</span></span>
<span data-ttu-id="5b41f-114">이 cmdlet이 가져오는 확장의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b41f-114">Specifies the name of the extension that this cmdlet gets.</span></span>

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

### <span data-ttu-id="5b41f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b41f-115">-ResourceGroupName</span></span>
<span data-ttu-id="5b41f-116">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b41f-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="5b41f-117">-상태</span><span class="sxs-lookup"><span data-stu-id="5b41f-117">-Status</span></span>
<span data-ttu-id="5b41f-118">이 cmdlet이 확장의 인스턴스 보기만을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5b41f-118">Indicates that this cmdlet gets only the instance view of the extension.</span></span>

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

### <span data-ttu-id="5b41f-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="5b41f-119">-VMName</span></span>
<span data-ttu-id="5b41f-120">가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b41f-120">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="5b41f-121">이 cmdlet은이 매개 변수에서 지정 하는 가상 컴퓨터에 대 한 VMAccess에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5b41f-121">This cmdlet gets information about VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="5b41f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b41f-122">CommonParameters</span></span>
<span data-ttu-id="5b41f-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b41f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b41f-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b41f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b41f-125">입력</span><span class="sxs-lookup"><span data-stu-id="5b41f-125">INPUTS</span></span>

### <span data-ttu-id="5b41f-126">않아야</span><span class="sxs-lookup"><span data-stu-id="5b41f-126">None</span></span>
<span data-ttu-id="5b41f-127">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5b41f-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5b41f-128">출력</span><span class="sxs-lookup"><span data-stu-id="5b41f-128">OUTPUTS</span></span>

## <span data-ttu-id="5b41f-129">상속자</span><span class="sxs-lookup"><span data-stu-id="5b41f-129">NOTES</span></span>

## <span data-ttu-id="5b41f-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5b41f-130">RELATED LINKS</span></span>

[<span data-ttu-id="5b41f-131">제거-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="5b41f-131">Remove-AzureRmVMAccessExtension</span></span>](./Remove-AzureRmVMAccessExtension.md)

[<span data-ttu-id="5b41f-132">Set-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="5b41f-132">Set-AzureRmVMAccessExtension</span></span>](./Set-AzureRmVMAccessExtension.md)

[<span data-ttu-id="5b41f-133">Get-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="5b41f-133">Get-AzureRmVMExtension</span></span>](./Get-AzureRmVMExtension.md)


