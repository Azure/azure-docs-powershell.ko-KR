---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: 5029179A-99A5-4350-A8E5-D15ABA59CC93
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devtestlabs/get-azurermdtlvmsperuserpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlVMsPerUserPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlVMsPerUserPolicy.md
ms.openlocfilehash: 4d8bf2922d58190e41e71e17c96ab55b5ee9433f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529596"
---
# <span data-ttu-id="66dde-101">Get-AzureRmDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="66dde-101">Get-AzureRmDtlVMsPerUserPolicy</span></span>

## <span data-ttu-id="66dde-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66dde-102">SYNOPSIS</span></span>
<span data-ttu-id="66dde-103">DevTest 랩에서 랩에서 사용자 별 가상 컴퓨터 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="66dde-103">Gets the virtual machines per user policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66dde-104">구문과</span><span class="sxs-lookup"><span data-stu-id="66dde-104">SYNTAX</span></span>

```
Get-AzureRmDtlVMsPerUserPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66dde-105">설명은</span><span class="sxs-lookup"><span data-stu-id="66dde-105">DESCRIPTION</span></span>
<span data-ttu-id="66dde-106">**AzureRmDtlVMsPerUserPolicy** cmdlet은 사용자 당 허용 되는 최대 가상 컴퓨터 수를 설정할 수 있는 랩의 사용자 정책 별 가상 컴퓨터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="66dde-106">The **Get-AzureRmDtlVMsPerUserPolicy** cmdlet gets the virtual machines per user policy of a lab, which allows you to set the maximum number of virtual machines allowed per user.</span></span>
<span data-ttu-id="66dde-107">Cmdlet은 정책의 사용 또는 사용 안 함 상태와 정책에서 설정한 사용자 당 최대 가상 컴퓨터 수를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="66dde-107">The cmdlet returns the enabled or disabled status of the policy and the maximum number of virtual machines allowed per user that you have set in the policy.</span></span>

## <span data-ttu-id="66dde-108">예제의</span><span class="sxs-lookup"><span data-stu-id="66dde-108">EXAMPLES</span></span>

## <span data-ttu-id="66dde-109">변수</span><span class="sxs-lookup"><span data-stu-id="66dde-109">PARAMETERS</span></span>

### <span data-ttu-id="66dde-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66dde-110">-DefaultProfile</span></span>
<span data-ttu-id="66dde-111">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="66dde-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="66dde-112">-시 이름</span><span class="sxs-lookup"><span data-stu-id="66dde-112">-LabName</span></span>
<span data-ttu-id="66dde-113">이 cmdlet이 사용자 당 가상 컴퓨터 정책을 가져오는 랩의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="66dde-113">Specifies the name of the lab for which this cmdlet gets the virtual machine per user policy.</span></span>

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

### <span data-ttu-id="66dde-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66dde-114">-ResourceGroupName</span></span>
<span data-ttu-id="66dde-115">랩이 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="66dde-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="66dde-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66dde-116">CommonParameters</span></span>
<span data-ttu-id="66dde-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="66dde-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66dde-118">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66dde-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66dde-119">입력</span><span class="sxs-lookup"><span data-stu-id="66dde-119">INPUTS</span></span>

### <span data-ttu-id="66dde-120">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="66dde-120">System.String</span></span>

## <span data-ttu-id="66dde-121">출력</span><span class="sxs-lookup"><span data-stu-id="66dde-121">OUTPUTS</span></span>

### <span data-ttu-id="66dde-122">Microsoft. DevTestLabs. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="66dde-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="66dde-123">상속자</span><span class="sxs-lookup"><span data-stu-id="66dde-123">NOTES</span></span>

## <span data-ttu-id="66dde-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="66dde-124">RELATED LINKS</span></span>

[<span data-ttu-id="66dde-125">Set-AzureRmDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="66dde-125">Set-AzureRmDtlVMsPerUserPolicy</span></span>](./Set-AzureRmDtlVMsPerUserPolicy.md)


