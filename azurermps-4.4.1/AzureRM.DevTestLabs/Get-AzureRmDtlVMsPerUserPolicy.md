---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: 5029179A-99A5-4350-A8E5-D15ABA59CC93
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlVMsPerUserPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlVMsPerUserPolicy.md
ms.openlocfilehash: 2be26f222be7ec444706fb15fb862a43dc8b8116
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534120"
---
# <span data-ttu-id="83ee5-101">Get-AzureRmDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="83ee5-101">Get-AzureRmDtlVMsPerUserPolicy</span></span>

## <span data-ttu-id="83ee5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83ee5-102">SYNOPSIS</span></span>
<span data-ttu-id="83ee5-103">DevTest 랩에서 랩에서 사용자 별 가상 컴퓨터 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="83ee5-103">Gets the virtual machines per user policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="83ee5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="83ee5-104">SYNTAX</span></span>

```
Get-AzureRmDtlVMsPerUserPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83ee5-105">설명은</span><span class="sxs-lookup"><span data-stu-id="83ee5-105">DESCRIPTION</span></span>
<span data-ttu-id="83ee5-106">**AzureRmDtlVMsPerUserPolicy** cmdlet은 사용자 당 허용 되는 최대 가상 컴퓨터 수를 설정할 수 있는 랩의 사용자 정책 별 가상 컴퓨터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="83ee5-106">The **Get-AzureRmDtlVMsPerUserPolicy** cmdlet gets the virtual machines per user policy of a lab, which allows you to set the maximum number of virtual machines allowed per user.</span></span>
<span data-ttu-id="83ee5-107">Cmdlet은 정책의 사용 또는 사용 안 함 상태와 정책에서 설정한 사용자 당 최대 가상 컴퓨터 수를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="83ee5-107">The cmdlet returns the enabled or disabled status of the policy and the maximum number of virtual machines allowed per user that you have set in the policy.</span></span>

## <span data-ttu-id="83ee5-108">예제의</span><span class="sxs-lookup"><span data-stu-id="83ee5-108">EXAMPLES</span></span>

## <span data-ttu-id="83ee5-109">변수</span><span class="sxs-lookup"><span data-stu-id="83ee5-109">PARAMETERS</span></span>

### <span data-ttu-id="83ee5-110">-시 이름</span><span class="sxs-lookup"><span data-stu-id="83ee5-110">-LabName</span></span>
<span data-ttu-id="83ee5-111">이 cmdlet이 사용자 당 가상 컴퓨터 정책을 가져오는 랩의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="83ee5-111">Specifies the name of the lab for which this cmdlet gets the virtual machine per user policy.</span></span>

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

### <span data-ttu-id="83ee5-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83ee5-112">-ResourceGroupName</span></span>
<span data-ttu-id="83ee5-113">랩이 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="83ee5-113">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="83ee5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83ee5-114">-DefaultProfile</span></span>
<span data-ttu-id="83ee5-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="83ee5-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83ee5-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83ee5-116">CommonParameters</span></span>
<span data-ttu-id="83ee5-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="83ee5-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83ee5-118">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83ee5-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83ee5-119">입력</span><span class="sxs-lookup"><span data-stu-id="83ee5-119">INPUTS</span></span>

## <span data-ttu-id="83ee5-120">출력</span><span class="sxs-lookup"><span data-stu-id="83ee5-120">OUTPUTS</span></span>

### <span data-ttu-id="83ee5-121">Microsoft. DevTestLabs. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="83ee5-121">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>
<span data-ttu-id="83ee5-122">이 cmdlet은 랩에서 사용자가 만들 수 있는 최대 가상 컴퓨터 수를 지정 하는 정책을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="83ee5-122">This cmdlet returns the policy that specifies the maximum number of virtual machines that can be created by a user in the lab.</span></span>

## <span data-ttu-id="83ee5-123">상속자</span><span class="sxs-lookup"><span data-stu-id="83ee5-123">NOTES</span></span>

## <span data-ttu-id="83ee5-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="83ee5-124">RELATED LINKS</span></span>

[<span data-ttu-id="83ee5-125">Set-AzureRmDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="83ee5-125">Set-AzureRmDtlVMsPerUserPolicy</span></span>](./Set-AzureRmDtlVMsPerUserPolicy.md)


