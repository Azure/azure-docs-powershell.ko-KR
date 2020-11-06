---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 1017A74D-6420-4E51-A4A4-1AD3AD6D8122
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMCustomScriptExtension.md
ms.openlocfilehash: 1f348a7cddc31a2a3d3d255aa6b4fe80d1808f36
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529917"
---
# <span data-ttu-id="b18dd-101">Get-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="b18dd-101">Get-AzureRmVMCustomScriptExtension</span></span>

## <span data-ttu-id="b18dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b18dd-102">SYNOPSIS</span></span>
<span data-ttu-id="b18dd-103">사용자 지정 스크립트 확장에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b18dd-103">Gets information about a custom script extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b18dd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b18dd-104">SYNTAX</span></span>

```
Get-AzureRmVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [<CommonParameters>]
```

## <span data-ttu-id="b18dd-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b18dd-105">DESCRIPTION</span></span>
<span data-ttu-id="b18dd-106">**AzureRmVMCustomScriptExtension** cmdlet은 가상 컴퓨터의 사용자 지정 스크립트 가상 컴퓨터 확장에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b18dd-106">The **Get-AzureRmVMCustomScriptExtension** cmdlet gets information about a custom script Virtual Machine Extension on a virtual machine.</span></span>

## <span data-ttu-id="b18dd-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b18dd-107">EXAMPLES</span></span>

### <span data-ttu-id="b18dd-108">예제 1: 사용자 지정 스크립트 확장 가져오기</span><span class="sxs-lookup"><span data-stu-id="b18dd-108">Example 1: Get a custom script extension</span></span>
```
PS C:\> $VMCustomScriptExtension = Get-AzureRmVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoCustomScript"
```

<span data-ttu-id="b18dd-109">이 명령은 VirtualMachine07 이라는 가상 컴퓨터에 대해 ContosoCustomScript 이라는 사용자 지정 스크립트 확장을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b18dd-109">This command gets the custom script extension named ContosoCustomScript for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="b18dd-110">예제 2: 사용자 지정 스크립트 확장의 인스턴스 뷰 가져오기</span><span class="sxs-lookup"><span data-stu-id="b18dd-110">Example 2: Get the instance view of a custom script extension</span></span>
```
PS C:\> $VMCustomScriptExtension = Get-AzureRmVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoCustomScript" -Status
```

<span data-ttu-id="b18dd-111">이 명령은 VirtualMachine07 이라는 가상 컴퓨터에 대해 ContosoCustomScript 이라는 사용자 지정 스크립트 확장의 인스턴스 뷰를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b18dd-111">This command gets the instance view of the custom script extension named ContosoCustomScript for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="b18dd-112">변수</span><span class="sxs-lookup"><span data-stu-id="b18dd-112">PARAMETERS</span></span>

### <span data-ttu-id="b18dd-113">-이름</span><span class="sxs-lookup"><span data-stu-id="b18dd-113">-Name</span></span>
<span data-ttu-id="b18dd-114">이 cmdlet에 대 한 정보를 가져오는 사용자 지정 스크립트 확장의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b18dd-114">Specifies the name of the custom script extension about which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="b18dd-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b18dd-115">-ResourceGroupName</span></span>
<span data-ttu-id="b18dd-116">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b18dd-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="b18dd-117">-상태</span><span class="sxs-lookup"><span data-stu-id="b18dd-117">-Status</span></span>
<span data-ttu-id="b18dd-118">이 cmdlet이 사용자 지정 스크립트 확장의 인스턴스 뷰를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b18dd-118">Indicates that this cmdlet gets the instance view of the custom script extension.</span></span>

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

### <span data-ttu-id="b18dd-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="b18dd-119">-VMName</span></span>
<span data-ttu-id="b18dd-120">이 cmdlet이 사용자 지정 스크립트 확장을 가져오는 가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b18dd-120">Specifies the name of a virtual machine for which this cmdlet gets the custom script extension.</span></span>

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

### <span data-ttu-id="b18dd-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b18dd-121">CommonParameters</span></span>
<span data-ttu-id="b18dd-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b18dd-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b18dd-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b18dd-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b18dd-124">입력</span><span class="sxs-lookup"><span data-stu-id="b18dd-124">INPUTS</span></span>

### <span data-ttu-id="b18dd-125">않아야</span><span class="sxs-lookup"><span data-stu-id="b18dd-125">None</span></span>
<span data-ttu-id="b18dd-126">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b18dd-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b18dd-127">출력</span><span class="sxs-lookup"><span data-stu-id="b18dd-127">OUTPUTS</span></span>

## <span data-ttu-id="b18dd-128">상속자</span><span class="sxs-lookup"><span data-stu-id="b18dd-128">NOTES</span></span>

## <span data-ttu-id="b18dd-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b18dd-129">RELATED LINKS</span></span>

[<span data-ttu-id="b18dd-130">Get-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="b18dd-130">Get-AzureRmVMAccessExtension</span></span>](./Get-AzureRmVMAccessExtension.md)

[<span data-ttu-id="b18dd-131">Get-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="b18dd-131">Get-AzureRmVMExtension</span></span>](./Get-AzureRmVMExtension.md)

[<span data-ttu-id="b18dd-132">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="b18dd-132">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)


