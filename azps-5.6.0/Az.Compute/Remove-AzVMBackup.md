---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 2AB1B227-68C4-49AE-84C0-E1421E609DE7
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azvmbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMBackup.md
ms.openlocfilehash: 23ae31c79c33e9299d1cf3dc5998798657408da4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972091"
---
# <span data-ttu-id="0d2c9-101">Remove-AzVMBackup</span><span class="sxs-lookup"><span data-stu-id="0d2c9-101">Remove-AzVMBackup</span></span>

## <span data-ttu-id="0d2c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d2c9-102">SYNOPSIS</span></span>
<span data-ttu-id="0d2c9-103">가상 머신에서 백업을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0d2c9-103">Removes the backup from a virtual machine.</span></span>

## <span data-ttu-id="0d2c9-104">구문</span><span class="sxs-lookup"><span data-stu-id="0d2c9-104">SYNTAX</span></span>

```
Remove-AzVMBackup [-ResourceGroupName] <String> [-VMName] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d2c9-105">설명</span><span class="sxs-lookup"><span data-stu-id="0d2c9-105">DESCRIPTION</span></span>

## <span data-ttu-id="0d2c9-106">예제</span><span class="sxs-lookup"><span data-stu-id="0d2c9-106">EXAMPLES</span></span>

### <span data-ttu-id="0d2c9-107">1:</span><span class="sxs-lookup"><span data-stu-id="0d2c9-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="0d2c9-108">매개 변수</span><span class="sxs-lookup"><span data-stu-id="0d2c9-108">PARAMETERS</span></span>

### <span data-ttu-id="0d2c9-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d2c9-109">-DefaultProfile</span></span>
<span data-ttu-id="0d2c9-110">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0d2c9-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d2c9-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d2c9-111">-ResourceGroupName</span></span>
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

### <span data-ttu-id="0d2c9-112">-Tag</span><span class="sxs-lookup"><span data-stu-id="0d2c9-112">-Tag</span></span>
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

### <span data-ttu-id="0d2c9-113">-VMName</span><span class="sxs-lookup"><span data-stu-id="0d2c9-113">-VMName</span></span>
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

### <span data-ttu-id="0d2c9-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d2c9-114">CommonParameters</span></span>
<span data-ttu-id="0d2c9-115">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0d2c9-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d2c9-116">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0d2c9-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d2c9-117">입력</span><span class="sxs-lookup"><span data-stu-id="0d2c9-117">INPUTS</span></span>

### <span data-ttu-id="0d2c9-118">System.String</span><span class="sxs-lookup"><span data-stu-id="0d2c9-118">System.String</span></span>

## <span data-ttu-id="0d2c9-119">출력</span><span class="sxs-lookup"><span data-stu-id="0d2c9-119">OUTPUTS</span></span>

### <span data-ttu-id="0d2c9-120">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="0d2c9-120">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="0d2c9-121">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0d2c9-121">NOTES</span></span>

## <span data-ttu-id="0d2c9-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0d2c9-122">RELATED LINKS</span></span>
