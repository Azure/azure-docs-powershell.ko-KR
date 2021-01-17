---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3702701E-428D-47E2-A227-0F38B055F881
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMUsage.md
ms.openlocfilehash: d22e36ad3cc4737be9c73d6b7cdc49329f904263
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98332697"
---
# <span data-ttu-id="f105b-101">Get-AzVMUsage</span><span class="sxs-lookup"><span data-stu-id="f105b-101">Get-AzVMUsage</span></span>

## <span data-ttu-id="f105b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f105b-102">SYNOPSIS</span></span>
<span data-ttu-id="f105b-103">위치에 대한 가상 머신 코어 수 사용량을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f105b-103">Gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="f105b-104">구문</span><span class="sxs-lookup"><span data-stu-id="f105b-104">SYNTAX</span></span>

```
Get-AzVMUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f105b-105">설명</span><span class="sxs-lookup"><span data-stu-id="f105b-105">DESCRIPTION</span></span>
<span data-ttu-id="f105b-106">**Get-AzVMUsage** cmdlet은 위치에 대한 가상 머신 코어 수 사용량을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f105b-106">The **Get-AzVMUsage** cmdlet gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="f105b-107">예제</span><span class="sxs-lookup"><span data-stu-id="f105b-107">EXAMPLES</span></span>

### <span data-ttu-id="f105b-108">예제 1: 위치에 대한 코어 수 사용량을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f105b-108">Example 1: Get core count usage for a location</span></span>
```
PS C:\> Get-AzVMUsage -Location "Central US"
```

<span data-ttu-id="f105b-109">이 명령은 미국 중부 위치에 대한 가상 머신 코어 수 사용량을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f105b-109">This command gets the virtual machine core count usage for the location Central US.</span></span>

## <span data-ttu-id="f105b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f105b-110">PARAMETERS</span></span>

### <span data-ttu-id="f105b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f105b-111">-DefaultProfile</span></span>
<span data-ttu-id="f105b-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f105b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f105b-113">-Location</span><span class="sxs-lookup"><span data-stu-id="f105b-113">-Location</span></span>
<span data-ttu-id="f105b-114">이 cmdlet이 가상 머신 코어 수 사용량을 얻을 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f105b-114">Specifies the location for which this cmdlet gets virtual machine core count usage.</span></span>

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

### <span data-ttu-id="f105b-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f105b-115">CommonParameters</span></span>
<span data-ttu-id="f105b-116">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f105b-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f105b-117">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f105b-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f105b-118">입력</span><span class="sxs-lookup"><span data-stu-id="f105b-118">INPUTS</span></span>

### <span data-ttu-id="f105b-119">System.String</span><span class="sxs-lookup"><span data-stu-id="f105b-119">System.String</span></span>

## <span data-ttu-id="f105b-120">출력</span><span class="sxs-lookup"><span data-stu-id="f105b-120">OUTPUTS</span></span>

### <span data-ttu-id="f105b-121">Microsoft.Azure.Commands.Compute.Models.PSUsage</span><span class="sxs-lookup"><span data-stu-id="f105b-121">Microsoft.Azure.Commands.Compute.Models.PSUsage</span></span>

## <span data-ttu-id="f105b-122">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f105b-122">NOTES</span></span>

## <span data-ttu-id="f105b-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f105b-123">RELATED LINKS</span></span>

[<span data-ttu-id="f105b-124">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="f105b-124">Get-AzVM</span></span>](./Get-AzVM.md)


