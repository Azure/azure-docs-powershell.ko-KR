---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: B02CEAC8-C838-4890-8C21-9897CA39EF45
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmsqlserverextension
schema: 2.0.0
ms.openlocfilehash: aa37745469ad6610fa2511d49c3404bbf54d8059
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882326"
---
# <span data-ttu-id="c9fca-101">Remove-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="c9fca-101">Remove-AzureRmVMSqlServerExtension</span></span>

## <span data-ttu-id="c9fca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9fca-102">SYNOPSIS</span></span>
<span data-ttu-id="c9fca-103">가상 컴퓨터에서 SQL Server 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9fca-103">Removes a SQL Server extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9fca-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c9fca-104">SYNTAX</span></span>

```
Remove-AzureRmVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c9fca-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c9fca-105">DESCRIPTION</span></span>
<span data-ttu-id="c9fca-106">**AzureRmVMSqlServerExtension** cmdlet은 가상 머신에서 AzureSQL Server 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9fca-106">The **Remove-AzureRmVMSqlServerExtension** cmdlet removes an AzureSQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="c9fca-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c9fca-107">EXAMPLES</span></span>

### <span data-ttu-id="c9fca-108">예제 1: SQL Server 확장 제거</span><span class="sxs-lookup"><span data-stu-id="c9fca-108">Example 1: Remove a SQL Server extension</span></span>
```
PS C:\> Remove-AzureRMVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" -Name "SqlIaaSAgent"
```

<span data-ttu-id="c9fca-109">이 명령은 ContosoVM22 이라는 가상 컴퓨터에서 SQL Server 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9fca-109">This command removes a SQL Server extension from the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="c9fca-110">변수</span><span class="sxs-lookup"><span data-stu-id="c9fca-110">PARAMETERS</span></span>

### <span data-ttu-id="c9fca-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9fca-111">-DefaultProfile</span></span>
<span data-ttu-id="c9fca-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c9fca-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9fca-113">-이름</span><span class="sxs-lookup"><span data-stu-id="c9fca-113">-Name</span></span>
<span data-ttu-id="c9fca-114">이 cmdlet이 제거 하는 확장 하는 SQL Server의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9fca-114">Specifies the name of the SQL Server the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c9fca-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9fca-115">-ResourceGroupName</span></span>
<span data-ttu-id="c9fca-116">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9fca-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="c9fca-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="c9fca-117">-VMName</span></span>
<span data-ttu-id="c9fca-118">이 cmdlet에서 SQL Server 확장을 제거 하는 가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9fca-118">Specifies the name of the virtual machine from which this cmdlet removes the SQL Server extension.</span></span>

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

### <span data-ttu-id="c9fca-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9fca-119">CommonParameters</span></span>
<span data-ttu-id="c9fca-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9fca-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9fca-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9fca-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9fca-122">입력</span><span class="sxs-lookup"><span data-stu-id="c9fca-122">INPUTS</span></span>

### <span data-ttu-id="c9fca-123">않아야</span><span class="sxs-lookup"><span data-stu-id="c9fca-123">None</span></span>
<span data-ttu-id="c9fca-124">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c9fca-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c9fca-125">출력</span><span class="sxs-lookup"><span data-stu-id="c9fca-125">OUTPUTS</span></span>

### <span data-ttu-id="c9fca-126">이는 PSAzureOperationResponse를 계산 하는 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="c9fca-126">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="c9fca-127">상속자</span><span class="sxs-lookup"><span data-stu-id="c9fca-127">NOTES</span></span>

## <span data-ttu-id="c9fca-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c9fca-128">RELATED LINKS</span></span>

[<span data-ttu-id="c9fca-129">Get-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="c9fca-129">Get-AzureRmVMSqlServerExtension</span></span>](./Get-AzureRMVMSqlServerExtension.md)

[<span data-ttu-id="c9fca-130">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="c9fca-130">Set-AzureRmVMSqlServerExtension</span></span>](./Set-AzureRMVMSqlServerExtension.md)


