---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3702701E-428D-47E2-A227-0F38B055F881
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMUsage.md
ms.openlocfilehash: ef13cdfc9a137790c0d9aa842a0ba31841baa99b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013728"
---
# <span data-ttu-id="1d9ba-101">Get-AzVMUsage</span><span class="sxs-lookup"><span data-stu-id="1d9ba-101">Get-AzVMUsage</span></span>

## <span data-ttu-id="1d9ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d9ba-102">SYNOPSIS</span></span>
<span data-ttu-id="1d9ba-103">위치에 대한 가상 머신 코어 수 사용량을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1d9ba-103">Gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="1d9ba-104">구문</span><span class="sxs-lookup"><span data-stu-id="1d9ba-104">SYNTAX</span></span>

```
Get-AzVMUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1d9ba-105">설명</span><span class="sxs-lookup"><span data-stu-id="1d9ba-105">DESCRIPTION</span></span>
<span data-ttu-id="1d9ba-106">**Get-AzVMUsage** cmdlet은 위치에 대한 가상 머신 코어 수 사용량을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1d9ba-106">The **Get-AzVMUsage** cmdlet gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="1d9ba-107">예제</span><span class="sxs-lookup"><span data-stu-id="1d9ba-107">EXAMPLES</span></span>

### <span data-ttu-id="1d9ba-108">예제 1: 위치에 대한 코어 개수 사용량을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1d9ba-108">Example 1: Get core count usage for a location</span></span>
```
PS C:\> Get-AzVMUsage -Location "Central US"
```

<span data-ttu-id="1d9ba-109">이 명령은 미국 중부 위치에 대한 가상 머신 코어 수 사용량을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1d9ba-109">This command gets the virtual machine core count usage for the location Central US.</span></span>

## <span data-ttu-id="1d9ba-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="1d9ba-110">PARAMETERS</span></span>

### <span data-ttu-id="1d9ba-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d9ba-111">-DefaultProfile</span></span>
<span data-ttu-id="1d9ba-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1d9ba-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d9ba-113">-Location</span><span class="sxs-lookup"><span data-stu-id="1d9ba-113">-Location</span></span>
<span data-ttu-id="1d9ba-114">이 cmdlet에서 가상 머신 코어 개수 사용량을 얻을 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1d9ba-114">Specifies the location for which this cmdlet gets virtual machine core count usage.</span></span>

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

### <span data-ttu-id="1d9ba-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d9ba-115">CommonParameters</span></span>
<span data-ttu-id="1d9ba-116">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1d9ba-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d9ba-117">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1d9ba-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d9ba-118">입력</span><span class="sxs-lookup"><span data-stu-id="1d9ba-118">INPUTS</span></span>

### <span data-ttu-id="1d9ba-119">System.String</span><span class="sxs-lookup"><span data-stu-id="1d9ba-119">System.String</span></span>

## <span data-ttu-id="1d9ba-120">출력</span><span class="sxs-lookup"><span data-stu-id="1d9ba-120">OUTPUTS</span></span>

### <span data-ttu-id="1d9ba-121">Microsoft.Azure.Commands.Compute.Models.PSUsage</span><span class="sxs-lookup"><span data-stu-id="1d9ba-121">Microsoft.Azure.Commands.Compute.Models.PSUsage</span></span>

## <span data-ttu-id="1d9ba-122">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1d9ba-122">NOTES</span></span>

## <span data-ttu-id="1d9ba-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1d9ba-123">RELATED LINKS</span></span>

[<span data-ttu-id="1d9ba-124">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="1d9ba-124">Get-AzVM</span></span>](./Get-AzVM.md)


