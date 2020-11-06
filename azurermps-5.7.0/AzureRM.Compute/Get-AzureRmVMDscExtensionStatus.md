---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 695F224D-DA25-49F2-916E-25DA2A48A4A7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMDscExtensionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMDscExtensionStatus.md
ms.openlocfilehash: 7cb7f175cc15e7d4e0915b6af9ef6fe6bdfc74d9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526979"
---
# <span data-ttu-id="5bd8a-101">Get-AzureRmVMDscExtensionStatus</span><span class="sxs-lookup"><span data-stu-id="5bd8a-101">Get-AzureRmVMDscExtensionStatus</span></span>

## <span data-ttu-id="5bd8a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5bd8a-102">SYNOPSIS</span></span>
<span data-ttu-id="5bd8a-103">가상 컴퓨터에 대 한 DSC 확장 처리기의 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5bd8a-103">Gets the status of the DSC extension handler for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5bd8a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5bd8a-104">SYNTAX</span></span>

```
Get-AzureRmVMDscExtensionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="5bd8a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5bd8a-105">DESCRIPTION</span></span>
<span data-ttu-id="5bd8a-106">**AzureRmVMDscExtensionStatus** cmdlet은 리소스 그룹의 가상 컴퓨터에 대 한 DSC (원하는 상태 구성) 확장 처리기의 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5bd8a-106">The **Get-AzureRmVMDscExtensionStatus** cmdlet gets the status of the Desired State Configuration (DSC) extension handler for a virtual machine in a resource group.</span></span>
<span data-ttu-id="5bd8a-107">구성이 적용 되 면이 cmdlet은 Start-DscConfiguration cmdlet과 일치 하는 출력을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="5bd8a-107">When a configuration is applied this cmdlet produces output consistent with the Start-DscConfiguration cmdlet.</span></span>

## <span data-ttu-id="5bd8a-108">예제의</span><span class="sxs-lookup"><span data-stu-id="5bd8a-108">EXAMPLES</span></span>

## <span data-ttu-id="5bd8a-109">변수</span><span class="sxs-lookup"><span data-stu-id="5bd8a-109">PARAMETERS</span></span>

### <span data-ttu-id="5bd8a-110">-이름</span><span class="sxs-lookup"><span data-stu-id="5bd8a-110">-Name</span></span>
<span data-ttu-id="5bd8a-111">확장을 나타내는 Azure Resource Manager 리소스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5bd8a-111">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="5bd8a-112">Set-AzureRmVMDscExtension cmdlet은이 이름을 **AzureRmVMDscExtensionStatus** 에서 사용 하는 것과 동일한 값인 Microsoft Powershell로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5bd8a-112">The Set-AzureRmVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the same value that is used by **Get-AzureRmVMDscExtensionStatus**.</span></span>
<span data-ttu-id="5bd8a-113">Set cmdlet의 기본 이름을 변경 하거나 자원 관리자 서식 파일에서 다른 자원 이름을 사용 하는 경우에만이 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5bd8a-113">Specify this parameter only if you changed the default name in the Set cmdlet or used a different resource name in a Resource Manager template.</span></span>

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

### <span data-ttu-id="5bd8a-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5bd8a-114">-ResourceGroupName</span></span>
<span data-ttu-id="5bd8a-115">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5bd8a-115">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="5bd8a-116">-VMName</span><span class="sxs-lookup"><span data-stu-id="5bd8a-116">-VMName</span></span>
<span data-ttu-id="5bd8a-117">이 cmdlet이 DSC 확장 상태를 가져오는 가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5bd8a-117">Specifies the name of a virtual machine for which this cmdlet gets the DSC extension status.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bd8a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bd8a-118">CommonParameters</span></span>
<span data-ttu-id="5bd8a-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5bd8a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bd8a-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5bd8a-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bd8a-121">입력</span><span class="sxs-lookup"><span data-stu-id="5bd8a-121">INPUTS</span></span>

### <span data-ttu-id="5bd8a-122">않아야</span><span class="sxs-lookup"><span data-stu-id="5bd8a-122">None</span></span>
<span data-ttu-id="5bd8a-123">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5bd8a-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5bd8a-124">출력</span><span class="sxs-lookup"><span data-stu-id="5bd8a-124">OUTPUTS</span></span>

## <span data-ttu-id="5bd8a-125">상속자</span><span class="sxs-lookup"><span data-stu-id="5bd8a-125">NOTES</span></span>

## <span data-ttu-id="5bd8a-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5bd8a-126">RELATED LINKS</span></span>

[<span data-ttu-id="5bd8a-127">Set-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="5bd8a-127">Set-AzureRmVMDscExtension</span></span>](./Set-AzureRmVMDscExtension.md)


