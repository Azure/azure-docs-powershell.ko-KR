---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 2AB1B227-68C4-49AE-84C0-E1421E609DE7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMBackup.md
ms.openlocfilehash: 52abb3af83f7ee0d8724243c917e3aeb58592ac9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703389"
---
# <span data-ttu-id="45f06-101">Remove-AzureRmVMBackup</span><span class="sxs-lookup"><span data-stu-id="45f06-101">Remove-AzureRmVMBackup</span></span>

## <span data-ttu-id="45f06-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45f06-102">SYNOPSIS</span></span>
<span data-ttu-id="45f06-103">가상 머신에서 백업을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="45f06-103">Removes the backup from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45f06-104">구문과</span><span class="sxs-lookup"><span data-stu-id="45f06-104">SYNTAX</span></span>

```
Remove-AzureRmVMBackup [-ResourceGroupName] <String> [-VMName] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45f06-105">설명은</span><span class="sxs-lookup"><span data-stu-id="45f06-105">DESCRIPTION</span></span>

## <span data-ttu-id="45f06-106">예제의</span><span class="sxs-lookup"><span data-stu-id="45f06-106">EXAMPLES</span></span>

### <span data-ttu-id="45f06-107">raid-1</span><span class="sxs-lookup"><span data-stu-id="45f06-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="45f06-108">변수</span><span class="sxs-lookup"><span data-stu-id="45f06-108">PARAMETERS</span></span>

### <span data-ttu-id="45f06-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45f06-109">-DefaultProfile</span></span>
<span data-ttu-id="45f06-110">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="45f06-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45f06-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45f06-111">-ResourceGroupName</span></span>
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

### <span data-ttu-id="45f06-112">태그</span><span class="sxs-lookup"><span data-stu-id="45f06-112">-Tag</span></span>
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

### <span data-ttu-id="45f06-113">-VMName</span><span class="sxs-lookup"><span data-stu-id="45f06-113">-VMName</span></span>
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

### <span data-ttu-id="45f06-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45f06-114">CommonParameters</span></span>
<span data-ttu-id="45f06-115">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="45f06-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45f06-116">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45f06-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45f06-117">입력</span><span class="sxs-lookup"><span data-stu-id="45f06-117">INPUTS</span></span>

## <span data-ttu-id="45f06-118">출력</span><span class="sxs-lookup"><span data-stu-id="45f06-118">OUTPUTS</span></span>

## <span data-ttu-id="45f06-119">상속자</span><span class="sxs-lookup"><span data-stu-id="45f06-119">NOTES</span></span>

## <span data-ttu-id="45f06-120">관련 링크</span><span class="sxs-lookup"><span data-stu-id="45f06-120">RELATED LINKS</span></span>

