---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 869167AA-54F8-4A1C-AC08-5555A63EE1BC
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/get-azdtlallowedvmsizespolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAllowedVMSizesPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAllowedVMSizesPolicy.md
ms.openlocfilehash: 8e4fbc28d52e8431122b8593b68b909554df6dc9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215559"
---
# <span data-ttu-id="15e6a-101">Get-AzDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="15e6a-101">Get-AzDtlAllowedVMSizesPolicy</span></span>

## <span data-ttu-id="15e6a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15e6a-102">SYNOPSIS</span></span>
<span data-ttu-id="15e6a-103">DevTest 랩에서 랩에서 허용 되는 가상 컴퓨터 크기 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="15e6a-103">Gets the allowed virtual machine sizes policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="15e6a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="15e6a-104">SYNTAX</span></span>

```
Get-AzDtlAllowedVMSizesPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="15e6a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="15e6a-105">DESCRIPTION</span></span>
<span data-ttu-id="15e6a-106">**AzDtlAllowedVMSizesPolicy** cmdlet은 허용 되는 가상 컴퓨터 크기 정책을 가져와 랩에서 허용 되는 가상 컴퓨터 크기 목록을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="15e6a-106">The **Get-AzDtlAllowedVMSizesPolicy** cmdlet gets the allowed virtual machine sizes policy, which allows you to specify a list of virtual machine sizes allowed in the lab.</span></span>
<span data-ttu-id="15e6a-107">Cmdlet은 정책의 사용 또는 사용 안 함 상태와 지정 된 정책에서 설정한 허용 되는 모든 가상 컴퓨터 크기의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="15e6a-107">The cmdlet returns the enabled or disabled status of the policy and a list of all the allowed virtual machine sizes that you have set in the specified policy.</span></span>

## <span data-ttu-id="15e6a-108">예제의</span><span class="sxs-lookup"><span data-stu-id="15e6a-108">EXAMPLES</span></span>

## <span data-ttu-id="15e6a-109">변수</span><span class="sxs-lookup"><span data-stu-id="15e6a-109">PARAMETERS</span></span>

### <span data-ttu-id="15e6a-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15e6a-110">-DefaultProfile</span></span>
<span data-ttu-id="15e6a-111">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="15e6a-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="15e6a-112">-시 이름</span><span class="sxs-lookup"><span data-stu-id="15e6a-112">-LabName</span></span>
<span data-ttu-id="15e6a-113">이 cmdlet이 가상 컴퓨터 크기 정책을 가져오는 랩의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="15e6a-113">Specifies the name of the lab for which this cmdlet gets virtual machines size policy.</span></span>

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

### <span data-ttu-id="15e6a-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15e6a-114">-ResourceGroupName</span></span>
<span data-ttu-id="15e6a-115">랩이 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="15e6a-115">Specifies the name of the resource group that the lab belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15e6a-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15e6a-116">CommonParameters</span></span>
<span data-ttu-id="15e6a-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="15e6a-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15e6a-118">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15e6a-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15e6a-119">입력</span><span class="sxs-lookup"><span data-stu-id="15e6a-119">INPUTS</span></span>

### <span data-ttu-id="15e6a-120">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="15e6a-120">System.String</span></span>

## <span data-ttu-id="15e6a-121">출력</span><span class="sxs-lookup"><span data-stu-id="15e6a-121">OUTPUTS</span></span>

### <span data-ttu-id="15e6a-122">Microsoft. DevTestLabs. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="15e6a-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="15e6a-123">상속자</span><span class="sxs-lookup"><span data-stu-id="15e6a-123">NOTES</span></span>

## <span data-ttu-id="15e6a-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="15e6a-124">RELATED LINKS</span></span>

[<span data-ttu-id="15e6a-125">Set-AzDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="15e6a-125">Set-AzDtlAllowedVMSizesPolicy</span></span>](./Set-AzDtlAllowedVMSizesPolicy.md)


