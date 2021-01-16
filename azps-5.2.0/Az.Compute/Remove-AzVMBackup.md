---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 2AB1B227-68C4-49AE-84C0-E1421E609DE7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMBackup.md
ms.openlocfilehash: 85b7a873a921e7fd08055e1e3adc7c70831f8fa1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363833"
---
# <span data-ttu-id="b2060-101">Remove-AzVMBackup</span><span class="sxs-lookup"><span data-stu-id="b2060-101">Remove-AzVMBackup</span></span>

## <span data-ttu-id="b2060-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2060-102">SYNOPSIS</span></span>
<span data-ttu-id="b2060-103">가상 머신에서 백업을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="b2060-103">Removes the backup from a virtual machine.</span></span>

## <span data-ttu-id="b2060-104">구문</span><span class="sxs-lookup"><span data-stu-id="b2060-104">SYNTAX</span></span>

```
Remove-AzVMBackup [-ResourceGroupName] <String> [-VMName] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2060-105">설명</span><span class="sxs-lookup"><span data-stu-id="b2060-105">DESCRIPTION</span></span>

## <span data-ttu-id="b2060-106">예제</span><span class="sxs-lookup"><span data-stu-id="b2060-106">EXAMPLES</span></span>

### <span data-ttu-id="b2060-107">1:</span><span class="sxs-lookup"><span data-stu-id="b2060-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="b2060-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b2060-108">PARAMETERS</span></span>

### <span data-ttu-id="b2060-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2060-109">-DefaultProfile</span></span>
<span data-ttu-id="b2060-110">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b2060-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2060-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2060-111">-ResourceGroupName</span></span>
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

### <span data-ttu-id="b2060-112">-Tag</span><span class="sxs-lookup"><span data-stu-id="b2060-112">-Tag</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2060-113">-VMName</span><span class="sxs-lookup"><span data-stu-id="b2060-113">-VMName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2060-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2060-114">CommonParameters</span></span>
<span data-ttu-id="b2060-115">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b2060-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2060-116">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b2060-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2060-117">입력</span><span class="sxs-lookup"><span data-stu-id="b2060-117">INPUTS</span></span>

### <span data-ttu-id="b2060-118">System.String</span><span class="sxs-lookup"><span data-stu-id="b2060-118">System.String</span></span>

## <span data-ttu-id="b2060-119">출력</span><span class="sxs-lookup"><span data-stu-id="b2060-119">OUTPUTS</span></span>

### <span data-ttu-id="b2060-120">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="b2060-120">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="b2060-121">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b2060-121">NOTES</span></span>

## <span data-ttu-id="b2060-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b2060-122">RELATED LINKS</span></span>
