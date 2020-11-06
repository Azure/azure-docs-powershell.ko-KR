---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 842652D4-0F1C-4D0D-AB55-0D43D3C5D82A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMExtension.md
ms.openlocfilehash: 82ab2f02d47b17342f71b09eebe826fc48c07b81
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526976"
---
# <span data-ttu-id="f8553-101">Get-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="f8553-101">Get-AzureRmVMExtension</span></span>

## <span data-ttu-id="f8553-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8553-102">SYNOPSIS</span></span>
<span data-ttu-id="f8553-103">가상 컴퓨터에 설치 된 가상 컴퓨터 확장의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f8553-103">Gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8553-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f8553-104">SYNTAX</span></span>

```
Get-AzureRmVMExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [<CommonParameters>]
```

## <span data-ttu-id="f8553-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f8553-105">DESCRIPTION</span></span>
<span data-ttu-id="f8553-106">**AzureRmVMExtension** cmdlet은 가상 컴퓨터에 설치 된 가상 컴퓨터 확장의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f8553-106">The **Get-AzureRmVMExtension** cmdlet gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>
<span data-ttu-id="f8553-107">속성을 가져올 확장명의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8553-107">Specify the name of an extension for which to get properties.</span></span>
<span data-ttu-id="f8553-108">확장의 인스턴스 보기만 가져오려면 Status 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8553-108">To get only the instance view of an extension, specify the Status parameter.</span></span>

## <span data-ttu-id="f8553-109">예제의</span><span class="sxs-lookup"><span data-stu-id="f8553-109">EXAMPLES</span></span>

### <span data-ttu-id="f8553-110">예제 1: 확장의 속성 가져오기</span><span class="sxs-lookup"><span data-stu-id="f8553-110">Example 1: Get properties of an extension</span></span>
```
PS C:\> Get-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22" -Name "CustomScriptExtension"
```

<span data-ttu-id="f8553-111">이 명령은 리소스 그룹 ResourceGroup11의 VirtualMachine22 이라는 가상 컴퓨터에서 CustomScriptExtension 이라는 확장명에 대 한 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f8553-111">This command gets properties for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

### <span data-ttu-id="f8553-112">예제 2: 확장의 인스턴스 뷰 가져오기</span><span class="sxs-lookup"><span data-stu-id="f8553-112">Example 2: Get instance view of an extension</span></span>
```
PS C:\> Get-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Status
```

<span data-ttu-id="f8553-113">이 명령은 리소스 그룹 ResourceGroup11에 있는 VirtualMachine22 이라는 가상 컴퓨터에서 CustomScriptExtension 이라는 확장명에 대 한 인스턴스 보기를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f8553-113">This command gets the instance view for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="f8553-114">변수</span><span class="sxs-lookup"><span data-stu-id="f8553-114">PARAMETERS</span></span>

### <span data-ttu-id="f8553-115">-이름</span><span class="sxs-lookup"><span data-stu-id="f8553-115">-Name</span></span>
<span data-ttu-id="f8553-116">확장명의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8553-116">Specifies the name of an extension.</span></span>
<span data-ttu-id="f8553-117">이 cmdlet은이 매개 변수에서 지정 하는 확장에 대 한 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f8553-117">This cmdlet gets properties for the extension that this parameter specifies.</span></span>

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

### <span data-ttu-id="f8553-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8553-118">-ResourceGroupName</span></span>
<span data-ttu-id="f8553-119">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8553-119">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="f8553-120">-상태</span><span class="sxs-lookup"><span data-stu-id="f8553-120">-Status</span></span>
<span data-ttu-id="f8553-121">이 cmdlet이 확장의 인스턴스 보기만을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f8553-121">Indicates that this cmdlet gets only the instance view of an extension.</span></span>

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

### <span data-ttu-id="f8553-122">-VMName</span><span class="sxs-lookup"><span data-stu-id="f8553-122">-VMName</span></span>
<span data-ttu-id="f8553-123">가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8553-123">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="f8553-124">이 cmdlet은이 매개 변수에서 지정 하는 가상 컴퓨터에서 확장의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f8553-124">This cmdlet gets properties of an extension from the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="f8553-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8553-125">CommonParameters</span></span>
<span data-ttu-id="f8553-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8553-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8553-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8553-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8553-128">입력</span><span class="sxs-lookup"><span data-stu-id="f8553-128">INPUTS</span></span>

### <span data-ttu-id="f8553-129">않아야</span><span class="sxs-lookup"><span data-stu-id="f8553-129">None</span></span>
<span data-ttu-id="f8553-130">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f8553-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f8553-131">출력</span><span class="sxs-lookup"><span data-stu-id="f8553-131">OUTPUTS</span></span>

## <span data-ttu-id="f8553-132">상속자</span><span class="sxs-lookup"><span data-stu-id="f8553-132">NOTES</span></span>

## <span data-ttu-id="f8553-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f8553-133">RELATED LINKS</span></span>

[<span data-ttu-id="f8553-134">제거-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="f8553-134">Remove-AzureRmVMExtension</span></span>](./Remove-AzureRmVMExtension.md)

[<span data-ttu-id="f8553-135">Set-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="f8553-135">Set-AzureRmVMExtension</span></span>](./Set-AzureRmVMExtension.md)


