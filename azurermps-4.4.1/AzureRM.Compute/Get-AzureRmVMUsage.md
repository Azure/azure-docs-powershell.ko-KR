---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 3702701E-428D-47E2-A227-0F38B055F881
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMUsage.md
ms.openlocfilehash: af360334ab546685deadad45c2ea3f8954c226f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533115"
---
# <span data-ttu-id="6420f-101">Get-AzureRmVMUsage</span><span class="sxs-lookup"><span data-stu-id="6420f-101">Get-AzureRmVMUsage</span></span>

## <span data-ttu-id="6420f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6420f-102">SYNOPSIS</span></span>
<span data-ttu-id="6420f-103">위치에 대 한 가상 컴퓨터 코어 수 사용량을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6420f-103">Gets the virtual machine core count usage for a location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6420f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6420f-104">SYNTAX</span></span>

```
Get-AzureRmVMUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6420f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6420f-105">DESCRIPTION</span></span>
<span data-ttu-id="6420f-106">**AzureRmVMUsage** cmdlet은 위치에 대 한 가상 컴퓨터 코어 수 사용량을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6420f-106">The **Get-AzureRmVMUsage** cmdlet gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="6420f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="6420f-107">EXAMPLES</span></span>

### <span data-ttu-id="6420f-108">예제 1: 위치에 대 한 코어 카운트 사용 가져오기</span><span class="sxs-lookup"><span data-stu-id="6420f-108">Example 1: Get core count usage for a location</span></span>
```
PS C:\> Get-AzureRmVMUsage -Location "Central US"
```

<span data-ttu-id="6420f-109">이 명령은 위치 중앙 미국에 대 한 가상 컴퓨터 코어 수 사용량을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6420f-109">This command gets the virtual machine core count usage for the location Central US.</span></span>

## <span data-ttu-id="6420f-110">변수</span><span class="sxs-lookup"><span data-stu-id="6420f-110">PARAMETERS</span></span>

### <span data-ttu-id="6420f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6420f-111">-DefaultProfile</span></span>
<span data-ttu-id="6420f-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6420f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6420f-113">-위치</span><span class="sxs-lookup"><span data-stu-id="6420f-113">-Location</span></span>
<span data-ttu-id="6420f-114">이 cmdlet이 가상 컴퓨터 코어 수 사용량을 가져오는 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6420f-114">Specifies the location for which this cmdlet gets virtual machine core count usage.</span></span>

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

### <span data-ttu-id="6420f-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6420f-115">CommonParameters</span></span>
<span data-ttu-id="6420f-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6420f-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6420f-117">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6420f-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6420f-118">입력</span><span class="sxs-lookup"><span data-stu-id="6420f-118">INPUTS</span></span>

## <span data-ttu-id="6420f-119">출력</span><span class="sxs-lookup"><span data-stu-id="6420f-119">OUTPUTS</span></span>

## <span data-ttu-id="6420f-120">상속자</span><span class="sxs-lookup"><span data-stu-id="6420f-120">NOTES</span></span>

## <span data-ttu-id="6420f-121">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6420f-121">RELATED LINKS</span></span>

[<span data-ttu-id="6420f-122">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6420f-122">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


