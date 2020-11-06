---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: B02CEAC8-C838-4890-8C21-9897CA39EF45
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRMVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRMVMSqlServerExtension.md
ms.openlocfilehash: f074d61919098d6c23ab39424774d9ba18e457d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526944"
---
# <span data-ttu-id="baea3-101">Remove-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="baea3-101">Remove-AzureRmVMSqlServerExtension</span></span>

## <span data-ttu-id="baea3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="baea3-102">SYNOPSIS</span></span>
<span data-ttu-id="baea3-103">가상 컴퓨터에서 SQL Server 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="baea3-103">Removes a SQL Server extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="baea3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="baea3-104">SYNTAX</span></span>

```
Remove-AzureRmVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="baea3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="baea3-105">DESCRIPTION</span></span>
<span data-ttu-id="baea3-106">**AzureRmVMSqlServerExtension** cmdlet은 가상 머신에서 AzureSQL Server 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="baea3-106">The **Remove-AzureRmVMSqlServerExtension** cmdlet removes an AzureSQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="baea3-107">예제의</span><span class="sxs-lookup"><span data-stu-id="baea3-107">EXAMPLES</span></span>

### <span data-ttu-id="baea3-108">예제 1: SQL Server 확장 제거</span><span class="sxs-lookup"><span data-stu-id="baea3-108">Example 1: Remove a SQL Server extension</span></span>
```
PS C:\> Remove-AzureRMVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" -Name "SqlIaaSAgent"
```

<span data-ttu-id="baea3-109">이 명령은 ContosoVM22 이라는 가상 컴퓨터에서 SQL Server 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="baea3-109">This command removes a SQL Server extension from the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="baea3-110">변수</span><span class="sxs-lookup"><span data-stu-id="baea3-110">PARAMETERS</span></span>

### <span data-ttu-id="baea3-111">-이름</span><span class="sxs-lookup"><span data-stu-id="baea3-111">-Name</span></span>
<span data-ttu-id="baea3-112">이 cmdlet이 제거 하는 확장 하는 SQL Server의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="baea3-112">Specifies the name of the SQL Server the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="baea3-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="baea3-113">-ResourceGroupName</span></span>
<span data-ttu-id="baea3-114">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="baea3-114">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="baea3-115">-VMName</span><span class="sxs-lookup"><span data-stu-id="baea3-115">-VMName</span></span>
<span data-ttu-id="baea3-116">이 cmdlet에서 SQL Server 확장을 제거 하는 가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="baea3-116">Specifies the name of the virtual machine from which this cmdlet removes the SQL Server extension.</span></span>

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

### <span data-ttu-id="baea3-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="baea3-117">CommonParameters</span></span>
<span data-ttu-id="baea3-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="baea3-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="baea3-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="baea3-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="baea3-120">입력</span><span class="sxs-lookup"><span data-stu-id="baea3-120">INPUTS</span></span>

### <span data-ttu-id="baea3-121">않아야</span><span class="sxs-lookup"><span data-stu-id="baea3-121">None</span></span>
<span data-ttu-id="baea3-122">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="baea3-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="baea3-123">출력</span><span class="sxs-lookup"><span data-stu-id="baea3-123">OUTPUTS</span></span>

## <span data-ttu-id="baea3-124">상속자</span><span class="sxs-lookup"><span data-stu-id="baea3-124">NOTES</span></span>

## <span data-ttu-id="baea3-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="baea3-125">RELATED LINKS</span></span>

[<span data-ttu-id="baea3-126">Get-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="baea3-126">Get-AzureRmVMSqlServerExtension</span></span>](./Get-AzureRMVMSqlServerExtension.md)

[<span data-ttu-id="baea3-127">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="baea3-127">Set-AzureRmVMSqlServerExtension</span></span>](./Set-AzureRMVMSqlServerExtension.md)


