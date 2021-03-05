---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CBFFBF1B-1AF0-4D2F-9315-C3790A4E9346
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmbackupextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBackupExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBackupExtension.md
ms.openlocfilehash: 7be9116814af3f11e6bd61668b77df133676ab1a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013696"
---
# <span data-ttu-id="fa04c-101">Set-AzVMBackupExtension</span><span class="sxs-lookup"><span data-stu-id="fa04c-101">Set-AzVMBackupExtension</span></span>

## <span data-ttu-id="fa04c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa04c-102">SYNOPSIS</span></span>
<span data-ttu-id="fa04c-103">가상 머신에서 백업 확장 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="fa04c-103">Sets the backup extension properties on a virtual machine.</span></span>

## <span data-ttu-id="fa04c-104">구문</span><span class="sxs-lookup"><span data-stu-id="fa04c-104">SYNTAX</span></span>

```
Set-AzVMBackupExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fa04c-105">설명</span><span class="sxs-lookup"><span data-stu-id="fa04c-105">DESCRIPTION</span></span>

## <span data-ttu-id="fa04c-106">예제</span><span class="sxs-lookup"><span data-stu-id="fa04c-106">EXAMPLES</span></span>

### <span data-ttu-id="fa04c-107">1:</span><span class="sxs-lookup"><span data-stu-id="fa04c-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="fa04c-108">매개 변수</span><span class="sxs-lookup"><span data-stu-id="fa04c-108">PARAMETERS</span></span>

### <span data-ttu-id="fa04c-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa04c-109">-DefaultProfile</span></span>
<span data-ttu-id="fa04c-110">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fa04c-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fa04c-111">-Name</span><span class="sxs-lookup"><span data-stu-id="fa04c-111">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa04c-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa04c-112">-ResourceGroupName</span></span>
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

### <span data-ttu-id="fa04c-113">-Tag</span><span class="sxs-lookup"><span data-stu-id="fa04c-113">-Tag</span></span>
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

### <span data-ttu-id="fa04c-114">-VMName</span><span class="sxs-lookup"><span data-stu-id="fa04c-114">-VMName</span></span>
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

### <span data-ttu-id="fa04c-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa04c-115">CommonParameters</span></span>
<span data-ttu-id="fa04c-116">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fa04c-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa04c-117">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fa04c-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa04c-118">입력</span><span class="sxs-lookup"><span data-stu-id="fa04c-118">INPUTS</span></span>

### <span data-ttu-id="fa04c-119">System.String</span><span class="sxs-lookup"><span data-stu-id="fa04c-119">System.String</span></span>

## <span data-ttu-id="fa04c-120">출력</span><span class="sxs-lookup"><span data-stu-id="fa04c-120">OUTPUTS</span></span>

### <span data-ttu-id="fa04c-121">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="fa04c-121">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="fa04c-122">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fa04c-122">NOTES</span></span>

## <span data-ttu-id="fa04c-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fa04c-123">RELATED LINKS</span></span>
