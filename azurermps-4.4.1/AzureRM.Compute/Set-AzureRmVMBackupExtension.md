---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: CBFFBF1B-1AF0-4D2F-9315-C3790A4E9346
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMBackupExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMBackupExtension.md
ms.openlocfilehash: d95ef152ed21439aafdc1cf9778b101473539b19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525587"
---
# <span data-ttu-id="c0ac6-101">Set-AzureRmVMBackupExtension</span><span class="sxs-lookup"><span data-stu-id="c0ac6-101">Set-AzureRmVMBackupExtension</span></span>

## <span data-ttu-id="c0ac6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0ac6-102">SYNOPSIS</span></span>
<span data-ttu-id="c0ac6-103">가상 컴퓨터의 백업 확장 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0ac6-103">Sets the backup extension properties on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0ac6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c0ac6-104">SYNTAX</span></span>

```
Set-AzureRmVMBackupExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c0ac6-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c0ac6-105">DESCRIPTION</span></span>

## <span data-ttu-id="c0ac6-106">예제의</span><span class="sxs-lookup"><span data-stu-id="c0ac6-106">EXAMPLES</span></span>

### <span data-ttu-id="c0ac6-107">raid-1</span><span class="sxs-lookup"><span data-stu-id="c0ac6-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="c0ac6-108">변수</span><span class="sxs-lookup"><span data-stu-id="c0ac6-108">PARAMETERS</span></span>

### <span data-ttu-id="c0ac6-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0ac6-109">-DefaultProfile</span></span>
<span data-ttu-id="c0ac6-110">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c0ac6-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0ac6-111">-이름</span><span class="sxs-lookup"><span data-stu-id="c0ac6-111">-Name</span></span>
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

### <span data-ttu-id="c0ac6-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0ac6-112">-ResourceGroupName</span></span>
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

### <span data-ttu-id="c0ac6-113">태그</span><span class="sxs-lookup"><span data-stu-id="c0ac6-113">-Tag</span></span>
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

### <span data-ttu-id="c0ac6-114">-VMName</span><span class="sxs-lookup"><span data-stu-id="c0ac6-114">-VMName</span></span>
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

### <span data-ttu-id="c0ac6-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0ac6-115">CommonParameters</span></span>
<span data-ttu-id="c0ac6-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0ac6-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0ac6-117">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0ac6-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0ac6-118">입력</span><span class="sxs-lookup"><span data-stu-id="c0ac6-118">INPUTS</span></span>

## <span data-ttu-id="c0ac6-119">출력</span><span class="sxs-lookup"><span data-stu-id="c0ac6-119">OUTPUTS</span></span>

## <span data-ttu-id="c0ac6-120">상속자</span><span class="sxs-lookup"><span data-stu-id="c0ac6-120">NOTES</span></span>

## <span data-ttu-id="c0ac6-121">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c0ac6-121">RELATED LINKS</span></span>

