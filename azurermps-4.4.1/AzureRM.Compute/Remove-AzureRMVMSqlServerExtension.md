---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: B02CEAC8-C838-4890-8C21-9897CA39EF45
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRMVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRMVMSqlServerExtension.md
ms.openlocfilehash: 19d4022fcf5f3eee0ee8d77e7c061ae2f8d00629
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536435"
---
# <span data-ttu-id="cee50-101">Remove-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="cee50-101">Remove-AzureRmVMSqlServerExtension</span></span>

## <span data-ttu-id="cee50-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cee50-102">SYNOPSIS</span></span>
<span data-ttu-id="cee50-103">가상 컴퓨터에서 SQL Server 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="cee50-103">Removes a SQL Server extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cee50-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cee50-104">SYNTAX</span></span>

```
Remove-AzureRmVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cee50-105">설명은</span><span class="sxs-lookup"><span data-stu-id="cee50-105">DESCRIPTION</span></span>
<span data-ttu-id="cee50-106">**AzureRmVMSqlServerExtension** cmdlet은 가상 머신에서 AzureSQL Server 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="cee50-106">The **Remove-AzureRmVMSqlServerExtension** cmdlet removes an AzureSQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="cee50-107">예제의</span><span class="sxs-lookup"><span data-stu-id="cee50-107">EXAMPLES</span></span>

### <span data-ttu-id="cee50-108">예제 1: SQL Server 확장 제거</span><span class="sxs-lookup"><span data-stu-id="cee50-108">Example 1: Remove a SQL Server extension</span></span>
```
PS C:\> Remove-AzureRMVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" -Name "SqlIaaSAgent"
```

<span data-ttu-id="cee50-109">이 명령은 ContosoVM22 이라는 가상 컴퓨터에서 SQL Server 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="cee50-109">This command removes a SQL Server extension from the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="cee50-110">변수</span><span class="sxs-lookup"><span data-stu-id="cee50-110">PARAMETERS</span></span>

### <span data-ttu-id="cee50-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cee50-111">-DefaultProfile</span></span>
<span data-ttu-id="cee50-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cee50-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cee50-113">-이름</span><span class="sxs-lookup"><span data-stu-id="cee50-113">-Name</span></span>
<span data-ttu-id="cee50-114">이 cmdlet이 제거 하는 확장 하는 SQL Server의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cee50-114">Specifies the name of the SQL Server the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="cee50-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cee50-115">-ResourceGroupName</span></span>
<span data-ttu-id="cee50-116">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cee50-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="cee50-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="cee50-117">-VMName</span></span>
<span data-ttu-id="cee50-118">이 cmdlet에서 SQL Server 확장을 제거 하는 가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cee50-118">Specifies the name of the virtual machine from which this cmdlet removes the SQL Server extension.</span></span>

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

### <span data-ttu-id="cee50-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cee50-119">CommonParameters</span></span>
<span data-ttu-id="cee50-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cee50-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cee50-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cee50-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cee50-122">입력</span><span class="sxs-lookup"><span data-stu-id="cee50-122">INPUTS</span></span>

## <span data-ttu-id="cee50-123">출력</span><span class="sxs-lookup"><span data-stu-id="cee50-123">OUTPUTS</span></span>

## <span data-ttu-id="cee50-124">상속자</span><span class="sxs-lookup"><span data-stu-id="cee50-124">NOTES</span></span>

## <span data-ttu-id="cee50-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cee50-125">RELATED LINKS</span></span>

[<span data-ttu-id="cee50-126">Get-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="cee50-126">Get-AzureRmVMSqlServerExtension</span></span>](./Get-AzureRMVMSqlServerExtension.md)

[<span data-ttu-id="cee50-127">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="cee50-127">Set-AzureRmVMSqlServerExtension</span></span>](./Set-AzureRMVMSqlServerExtension.md)


