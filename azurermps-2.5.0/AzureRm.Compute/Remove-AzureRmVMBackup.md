---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 2AB1B227-68C4-49AE-84C0-E1421E609DE7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmbackup
schema: 2.0.0
ms.openlocfilehash: 8805d5da061ef19037768b72c08145e45c8f2a9c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882286"
---
# <span data-ttu-id="078d1-101">Remove-AzureRmVMBackup</span><span class="sxs-lookup"><span data-stu-id="078d1-101">Remove-AzureRmVMBackup</span></span>

## <span data-ttu-id="078d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="078d1-102">SYNOPSIS</span></span>
<span data-ttu-id="078d1-103">가상 머신에서 백업을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="078d1-103">Removes the backup from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="078d1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="078d1-104">SYNTAX</span></span>

```
Remove-AzureRmVMBackup [-ResourceGroupName] <String> [-VMName] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="078d1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="078d1-105">DESCRIPTION</span></span>

## <span data-ttu-id="078d1-106">예제의</span><span class="sxs-lookup"><span data-stu-id="078d1-106">EXAMPLES</span></span>

### <span data-ttu-id="078d1-107">raid-1</span><span class="sxs-lookup"><span data-stu-id="078d1-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="078d1-108">변수</span><span class="sxs-lookup"><span data-stu-id="078d1-108">PARAMETERS</span></span>

### <span data-ttu-id="078d1-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="078d1-109">-DefaultProfile</span></span>
<span data-ttu-id="078d1-110">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="078d1-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="078d1-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="078d1-111">-ResourceGroupName</span></span>
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

### <span data-ttu-id="078d1-112">태그</span><span class="sxs-lookup"><span data-stu-id="078d1-112">-Tag</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="078d1-113">-VMName</span><span class="sxs-lookup"><span data-stu-id="078d1-113">-VMName</span></span>
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

### <span data-ttu-id="078d1-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="078d1-114">CommonParameters</span></span>
<span data-ttu-id="078d1-115">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="078d1-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="078d1-116">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="078d1-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="078d1-117">입력</span><span class="sxs-lookup"><span data-stu-id="078d1-117">INPUTS</span></span>

### <span data-ttu-id="078d1-118">않아야</span><span class="sxs-lookup"><span data-stu-id="078d1-118">None</span></span>
<span data-ttu-id="078d1-119">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="078d1-119">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="078d1-120">출력</span><span class="sxs-lookup"><span data-stu-id="078d1-120">OUTPUTS</span></span>

### <span data-ttu-id="078d1-121">이는 PSAzureOperationResponse를 계산 하는 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="078d1-121">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="078d1-122">상속자</span><span class="sxs-lookup"><span data-stu-id="078d1-122">NOTES</span></span>

## <span data-ttu-id="078d1-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="078d1-123">RELATED LINKS</span></span>

