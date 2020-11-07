---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: CBFFBF1B-1AF0-4D2F-9315-C3790A4E9346
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmbackupextension
schema: 2.0.0
ms.openlocfilehash: 5d31ad189dcc5337b81373d52a026e01f93f08a7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881918"
---
# <span data-ttu-id="1507e-101">Set-AzureRmVMBackupExtension</span><span class="sxs-lookup"><span data-stu-id="1507e-101">Set-AzureRmVMBackupExtension</span></span>

## <span data-ttu-id="1507e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1507e-102">SYNOPSIS</span></span>
<span data-ttu-id="1507e-103">가상 컴퓨터의 백업 확장 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1507e-103">Sets the backup extension properties on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1507e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1507e-104">SYNTAX</span></span>

```
Set-AzureRmVMBackupExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1507e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1507e-105">DESCRIPTION</span></span>

## <span data-ttu-id="1507e-106">예제의</span><span class="sxs-lookup"><span data-stu-id="1507e-106">EXAMPLES</span></span>

### <span data-ttu-id="1507e-107">raid-1</span><span class="sxs-lookup"><span data-stu-id="1507e-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="1507e-108">변수</span><span class="sxs-lookup"><span data-stu-id="1507e-108">PARAMETERS</span></span>

### <span data-ttu-id="1507e-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1507e-109">-DefaultProfile</span></span>
<span data-ttu-id="1507e-110">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1507e-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1507e-111">-이름</span><span class="sxs-lookup"><span data-stu-id="1507e-111">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1507e-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1507e-112">-ResourceGroupName</span></span>
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

### <span data-ttu-id="1507e-113">태그</span><span class="sxs-lookup"><span data-stu-id="1507e-113">-Tag</span></span>
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

### <span data-ttu-id="1507e-114">-VMName</span><span class="sxs-lookup"><span data-stu-id="1507e-114">-VMName</span></span>
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

### <span data-ttu-id="1507e-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1507e-115">CommonParameters</span></span>
<span data-ttu-id="1507e-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1507e-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1507e-117">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1507e-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1507e-118">입력</span><span class="sxs-lookup"><span data-stu-id="1507e-118">INPUTS</span></span>

### <span data-ttu-id="1507e-119">않아야</span><span class="sxs-lookup"><span data-stu-id="1507e-119">None</span></span>
<span data-ttu-id="1507e-120">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1507e-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1507e-121">출력</span><span class="sxs-lookup"><span data-stu-id="1507e-121">OUTPUTS</span></span>

### <span data-ttu-id="1507e-122">이는 PSAzureOperationResponse를 계산 하는 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="1507e-122">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="1507e-123">상속자</span><span class="sxs-lookup"><span data-stu-id="1507e-123">NOTES</span></span>

## <span data-ttu-id="1507e-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1507e-124">RELATED LINKS</span></span>

