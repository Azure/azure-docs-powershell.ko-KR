---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: CBFFBF1B-1AF0-4D2F-9315-C3790A4E9346
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmbackupextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMBackupExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMBackupExtension.md
ms.openlocfilehash: ce07d1a46fe0f13b18238d9e20fb1d4b28b7d861
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876886"
---
# <span data-ttu-id="9a51f-101">Set-AzVMBackupExtension</span><span class="sxs-lookup"><span data-stu-id="9a51f-101">Set-AzVMBackupExtension</span></span>

## <span data-ttu-id="9a51f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a51f-102">SYNOPSIS</span></span>
<span data-ttu-id="9a51f-103">가상 컴퓨터의 백업 확장 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a51f-103">Sets the backup extension properties on a virtual machine.</span></span>

## <span data-ttu-id="9a51f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9a51f-104">SYNTAX</span></span>

```
Set-AzVMBackupExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9a51f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9a51f-105">DESCRIPTION</span></span>

## <span data-ttu-id="9a51f-106">예제의</span><span class="sxs-lookup"><span data-stu-id="9a51f-106">EXAMPLES</span></span>

### <span data-ttu-id="9a51f-107">raid-1</span><span class="sxs-lookup"><span data-stu-id="9a51f-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="9a51f-108">변수</span><span class="sxs-lookup"><span data-stu-id="9a51f-108">PARAMETERS</span></span>

### <span data-ttu-id="9a51f-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a51f-109">-DefaultProfile</span></span>
<span data-ttu-id="9a51f-110">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9a51f-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9a51f-111">-이름</span><span class="sxs-lookup"><span data-stu-id="9a51f-111">-Name</span></span>
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

### <span data-ttu-id="9a51f-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a51f-112">-ResourceGroupName</span></span>
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

### <span data-ttu-id="9a51f-113">태그</span><span class="sxs-lookup"><span data-stu-id="9a51f-113">-Tag</span></span>
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

### <span data-ttu-id="9a51f-114">-VMName</span><span class="sxs-lookup"><span data-stu-id="9a51f-114">-VMName</span></span>
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

### <span data-ttu-id="9a51f-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a51f-115">CommonParameters</span></span>
<span data-ttu-id="9a51f-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a51f-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a51f-117">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a51f-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a51f-118">입력</span><span class="sxs-lookup"><span data-stu-id="9a51f-118">INPUTS</span></span>

### <span data-ttu-id="9a51f-119">않아야</span><span class="sxs-lookup"><span data-stu-id="9a51f-119">None</span></span>
<span data-ttu-id="9a51f-120">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9a51f-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9a51f-121">출력</span><span class="sxs-lookup"><span data-stu-id="9a51f-121">OUTPUTS</span></span>

### <span data-ttu-id="9a51f-122">이는 PSAzureOperationResponse를 계산 하는 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="9a51f-122">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="9a51f-123">상속자</span><span class="sxs-lookup"><span data-stu-id="9a51f-123">NOTES</span></span>

## <span data-ttu-id="9a51f-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9a51f-124">RELATED LINKS</span></span>

