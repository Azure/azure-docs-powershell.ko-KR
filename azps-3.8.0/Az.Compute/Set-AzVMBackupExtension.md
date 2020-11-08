---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CBFFBF1B-1AF0-4D2F-9315-C3790A4E9346
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmbackupextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBackupExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBackupExtension.md
ms.openlocfilehash: 9ead4b38575bc297a820bda61eb6faf0beaf80d4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034629"
---
# <span data-ttu-id="f1495-101">Set-AzVMBackupExtension</span><span class="sxs-lookup"><span data-stu-id="f1495-101">Set-AzVMBackupExtension</span></span>

## <span data-ttu-id="f1495-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1495-102">SYNOPSIS</span></span>
<span data-ttu-id="f1495-103">가상 컴퓨터의 백업 확장 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1495-103">Sets the backup extension properties on a virtual machine.</span></span>

## <span data-ttu-id="f1495-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f1495-104">SYNTAX</span></span>

```
Set-AzVMBackupExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1495-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f1495-105">DESCRIPTION</span></span>

## <span data-ttu-id="f1495-106">예제의</span><span class="sxs-lookup"><span data-stu-id="f1495-106">EXAMPLES</span></span>

### <span data-ttu-id="f1495-107">raid-1</span><span class="sxs-lookup"><span data-stu-id="f1495-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="f1495-108">변수</span><span class="sxs-lookup"><span data-stu-id="f1495-108">PARAMETERS</span></span>

### <span data-ttu-id="f1495-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1495-109">-DefaultProfile</span></span>
<span data-ttu-id="f1495-110">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f1495-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1495-111">-이름</span><span class="sxs-lookup"><span data-stu-id="f1495-111">-Name</span></span>
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

### <span data-ttu-id="f1495-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1495-112">-ResourceGroupName</span></span>
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

### <span data-ttu-id="f1495-113">태그</span><span class="sxs-lookup"><span data-stu-id="f1495-113">-Tag</span></span>
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

### <span data-ttu-id="f1495-114">-VMName</span><span class="sxs-lookup"><span data-stu-id="f1495-114">-VMName</span></span>
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

### <span data-ttu-id="f1495-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1495-115">CommonParameters</span></span>
<span data-ttu-id="f1495-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1495-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1495-117">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f1495-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1495-118">입력</span><span class="sxs-lookup"><span data-stu-id="f1495-118">INPUTS</span></span>

### <span data-ttu-id="f1495-119">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f1495-119">System.String</span></span>

## <span data-ttu-id="f1495-120">출력</span><span class="sxs-lookup"><span data-stu-id="f1495-120">OUTPUTS</span></span>

### <span data-ttu-id="f1495-121">이는 PSAzureOperationResponse를 계산 하는 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="f1495-121">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="f1495-122">상속자</span><span class="sxs-lookup"><span data-stu-id="f1495-122">NOTES</span></span>

## <span data-ttu-id="f1495-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f1495-123">RELATED LINKS</span></span>
