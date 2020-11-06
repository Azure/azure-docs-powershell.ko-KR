---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: 5029179A-99A5-4350-A8E5-D15ABA59CC93
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devtestlabs/get-azurermdtlvmsperuserpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlVMsPerUserPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlVMsPerUserPolicy.md
ms.openlocfilehash: 53afed94f9733c041df2c49ff1ec97a2fb8277f0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528969"
---
# <span data-ttu-id="0051a-101">Get-AzureRmDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="0051a-101">Get-AzureRmDtlVMsPerUserPolicy</span></span>

## <span data-ttu-id="0051a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0051a-102">SYNOPSIS</span></span>
<span data-ttu-id="0051a-103">DevTest 랩에서 랩에서 사용자 별 가상 컴퓨터 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0051a-103">Gets the virtual machines per user policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0051a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0051a-104">SYNTAX</span></span>

```
Get-AzureRmDtlVMsPerUserPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0051a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0051a-105">DESCRIPTION</span></span>
<span data-ttu-id="0051a-106">**AzureRmDtlVMsPerUserPolicy** cmdlet은 사용자 당 허용 되는 최대 가상 컴퓨터 수를 설정할 수 있는 랩의 사용자 정책 별 가상 컴퓨터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0051a-106">The **Get-AzureRmDtlVMsPerUserPolicy** cmdlet gets the virtual machines per user policy of a lab, which allows you to set the maximum number of virtual machines allowed per user.</span></span>
<span data-ttu-id="0051a-107">Cmdlet은 정책의 사용 또는 사용 안 함 상태와 정책에서 설정한 사용자 당 최대 가상 컴퓨터 수를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0051a-107">The cmdlet returns the enabled or disabled status of the policy and the maximum number of virtual machines allowed per user that you have set in the policy.</span></span>

## <span data-ttu-id="0051a-108">예제의</span><span class="sxs-lookup"><span data-stu-id="0051a-108">EXAMPLES</span></span>

## <span data-ttu-id="0051a-109">변수</span><span class="sxs-lookup"><span data-stu-id="0051a-109">PARAMETERS</span></span>

### <span data-ttu-id="0051a-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0051a-110">-DefaultProfile</span></span>
<span data-ttu-id="0051a-111">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="0051a-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0051a-112">-시 이름</span><span class="sxs-lookup"><span data-stu-id="0051a-112">-LabName</span></span>
<span data-ttu-id="0051a-113">이 cmdlet이 사용자 당 가상 컴퓨터 정책을 가져오는 랩의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0051a-113">Specifies the name of the lab for which this cmdlet gets the virtual machine per user policy.</span></span>

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

### <span data-ttu-id="0051a-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0051a-114">-ResourceGroupName</span></span>
<span data-ttu-id="0051a-115">랩이 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0051a-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="0051a-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0051a-116">CommonParameters</span></span>
<span data-ttu-id="0051a-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0051a-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0051a-118">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0051a-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0051a-119">입력</span><span class="sxs-lookup"><span data-stu-id="0051a-119">INPUTS</span></span>

### <span data-ttu-id="0051a-120">않아야</span><span class="sxs-lookup"><span data-stu-id="0051a-120">None</span></span>
<span data-ttu-id="0051a-121">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0051a-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0051a-122">출력</span><span class="sxs-lookup"><span data-stu-id="0051a-122">OUTPUTS</span></span>

### <span data-ttu-id="0051a-123">Microsoft. DevTestLabs. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="0051a-123">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>
<span data-ttu-id="0051a-124">이 cmdlet은 랩에서 사용자가 만들 수 있는 최대 가상 컴퓨터 수를 지정 하는 정책을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0051a-124">This cmdlet returns the policy that specifies the maximum number of virtual machines that can be created by a user in the lab.</span></span>

## <span data-ttu-id="0051a-125">상속자</span><span class="sxs-lookup"><span data-stu-id="0051a-125">NOTES</span></span>

## <span data-ttu-id="0051a-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0051a-126">RELATED LINKS</span></span>

[<span data-ttu-id="0051a-127">Set-AzureRmDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="0051a-127">Set-AzureRmDtlVMsPerUserPolicy</span></span>](./Set-AzureRmDtlVMsPerUserPolicy.md)


