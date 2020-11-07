---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: 869167AA-54F8-4A1C-AC08-5555A63EE1BC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devtestlabs/get-azurermdtlallowedvmsizespolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAllowedVMSizesPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAllowedVMSizesPolicy.md
ms.openlocfilehash: 25b3f15b6a71b54cbcab1a53f793a32da8b2173a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702534"
---
# <span data-ttu-id="a844b-101">Get-AzureRmDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="a844b-101">Get-AzureRmDtlAllowedVMSizesPolicy</span></span>

## <span data-ttu-id="a844b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a844b-102">SYNOPSIS</span></span>
<span data-ttu-id="a844b-103">DevTest 랩에서 랩에서 허용 되는 가상 컴퓨터 크기 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a844b-103">Gets the allowed virtual machine sizes policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a844b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a844b-104">SYNTAX</span></span>

```
Get-AzureRmDtlAllowedVMSizesPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a844b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a844b-105">DESCRIPTION</span></span>
<span data-ttu-id="a844b-106">**AzureRmDtlAllowedVMSizesPolicy** cmdlet은 허용 되는 가상 컴퓨터 크기 정책을 가져와 랩에서 허용 되는 가상 컴퓨터 크기 목록을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a844b-106">The **Get-AzureRmDtlAllowedVMSizesPolicy** cmdlet gets the allowed virtual machine sizes policy, which allows you to specify a list of virtual machine sizes allowed in the lab.</span></span>
<span data-ttu-id="a844b-107">Cmdlet은 정책의 사용 또는 사용 안 함 상태와 지정 된 정책에서 설정한 허용 되는 모든 가상 컴퓨터 크기의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a844b-107">The cmdlet returns the enabled or disabled status of the policy and a list of all the allowed virtual machine sizes that you have set in the specified policy.</span></span>

## <span data-ttu-id="a844b-108">예제의</span><span class="sxs-lookup"><span data-stu-id="a844b-108">EXAMPLES</span></span>

## <span data-ttu-id="a844b-109">변수</span><span class="sxs-lookup"><span data-stu-id="a844b-109">PARAMETERS</span></span>

### <span data-ttu-id="a844b-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a844b-110">-DefaultProfile</span></span>
<span data-ttu-id="a844b-111">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="a844b-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a844b-112">-시 이름</span><span class="sxs-lookup"><span data-stu-id="a844b-112">-LabName</span></span>
<span data-ttu-id="a844b-113">이 cmdlet이 가상 컴퓨터 크기 정책을 가져오는 랩의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a844b-113">Specifies the name of the lab for which this cmdlet gets virtual machines size policy.</span></span>

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

### <span data-ttu-id="a844b-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a844b-114">-ResourceGroupName</span></span>
<span data-ttu-id="a844b-115">랩이 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a844b-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="a844b-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a844b-116">CommonParameters</span></span>
<span data-ttu-id="a844b-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a844b-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a844b-118">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a844b-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a844b-119">입력</span><span class="sxs-lookup"><span data-stu-id="a844b-119">INPUTS</span></span>

### <span data-ttu-id="a844b-120">않아야</span><span class="sxs-lookup"><span data-stu-id="a844b-120">None</span></span>
<span data-ttu-id="a844b-121">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a844b-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a844b-122">출력</span><span class="sxs-lookup"><span data-stu-id="a844b-122">OUTPUTS</span></span>

### <span data-ttu-id="a844b-123">Microsoft. DevTestLabs. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="a844b-123">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>
<span data-ttu-id="a844b-124">이 cmdlet은 랩에서 허용 되는 가상 컴퓨터 크기 목록을 지정 하는 정책을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a844b-124">This cmdlet returns the policy that specifies the list of virtual machine sizes allowed in the lab.</span></span>

## <span data-ttu-id="a844b-125">상속자</span><span class="sxs-lookup"><span data-stu-id="a844b-125">NOTES</span></span>

## <span data-ttu-id="a844b-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a844b-126">RELATED LINKS</span></span>

[<span data-ttu-id="a844b-127">Set-AzureRmDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="a844b-127">Set-AzureRmDtlAllowedVMSizesPolicy</span></span>](./Set-AzureRmDtlAllowedVMSizesPolicy.md)

[<span data-ttu-id="a844b-128">Azure 개발 테스트 랩 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a844b-128">Azure Development Test Lab Cmdlets</span></span>](./AzureRM.DevTestLabs.md)


