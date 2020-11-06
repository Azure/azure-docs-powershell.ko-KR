---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: D5BEA683-44AE-4D71-827D-02A03F0BEAE9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRMVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRMVMDiagnosticsExtension.md
ms.openlocfilehash: 32d3d5a152f36c0e4e5f8e3e4e4ecc2b8eb6ee31
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530558"
---
# <span data-ttu-id="bf630-101">Get-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="bf630-101">Get-AzureRmVMDiagnosticsExtension</span></span>

## <span data-ttu-id="bf630-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf630-102">SYNOPSIS</span></span>
<span data-ttu-id="bf630-103">가상 컴퓨터의 진단 확장 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bf630-103">Gets the settings of the Diagnostics extension on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf630-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bf630-104">SYNTAX</span></span>

```
Get-AzureRmVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [<CommonParameters>]
```

## <span data-ttu-id="bf630-105">설명은</span><span class="sxs-lookup"><span data-stu-id="bf630-105">DESCRIPTION</span></span>
<span data-ttu-id="bf630-106">**AzureRmVMDiagnosticsExtension** cmdlet은 가상 컴퓨터에서 Azure Diagnostics 확장의 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bf630-106">The **Get-AzureRmVMDiagnosticsExtension** cmdlet gets the settings of the Azure Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="bf630-107">예제의</span><span class="sxs-lookup"><span data-stu-id="bf630-107">EXAMPLES</span></span>

### <span data-ttu-id="bf630-108">예제 1: 가상 컴퓨터에 적용 되는 진단 확장 기능 가져오기</span><span class="sxs-lookup"><span data-stu-id="bf630-108">Example 1: Get the diagnostics extension applied to a virtual machine</span></span>
```
PS C:\> Get-AzureRmVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22"
```

<span data-ttu-id="bf630-109">이 명령은 ContosoVM22 이라는 가상 컴퓨터에 적용 되는 진단 확장을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bf630-109">This command gets the diagnostics extension applied to the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="bf630-110">변수</span><span class="sxs-lookup"><span data-stu-id="bf630-110">PARAMETERS</span></span>

### <span data-ttu-id="bf630-111">-이름</span><span class="sxs-lookup"><span data-stu-id="bf630-111">-Name</span></span>
<span data-ttu-id="bf630-112">이 cmdlet에 대 한 설정을 가져오는 진단 확장의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf630-112">Specifies the name of the Diagnostics extension for which this cmdlet gets settings.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf630-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf630-113">-ResourceGroupName</span></span>
<span data-ttu-id="bf630-114">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf630-114">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="bf630-115">-상태</span><span class="sxs-lookup"><span data-stu-id="bf630-115">-Status</span></span>
<span data-ttu-id="bf630-116">이 cmdlet이 상태 값을 사용 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="bf630-116">Indicates that this cmdlet uses the Status value.</span></span>

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

### <span data-ttu-id="bf630-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="bf630-117">-VMName</span></span>
<span data-ttu-id="bf630-118">이 cmdlet이 진단 확장을 가져오는 가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf630-118">Specifies the name of the virtual machine from which this cmdlet gets the Diagnostics extension.</span></span>

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

### <span data-ttu-id="bf630-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf630-119">CommonParameters</span></span>
<span data-ttu-id="bf630-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf630-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf630-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf630-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf630-122">입력</span><span class="sxs-lookup"><span data-stu-id="bf630-122">INPUTS</span></span>

### <span data-ttu-id="bf630-123">않아야</span><span class="sxs-lookup"><span data-stu-id="bf630-123">None</span></span>
<span data-ttu-id="bf630-124">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bf630-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bf630-125">출력</span><span class="sxs-lookup"><span data-stu-id="bf630-125">OUTPUTS</span></span>

## <span data-ttu-id="bf630-126">상속자</span><span class="sxs-lookup"><span data-stu-id="bf630-126">NOTES</span></span>

## <span data-ttu-id="bf630-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bf630-127">RELATED LINKS</span></span>

[<span data-ttu-id="bf630-128">제거-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="bf630-128">Remove-AzureRmVMDiagnosticsExtension</span></span>](./Remove-AzureRmVMDiagnosticsExtension.md)

[<span data-ttu-id="bf630-129">Set-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="bf630-129">Set-AzureRmVMDiagnosticsExtension</span></span>](./Set-AzureRMVMDiagnosticsExtension.md)


