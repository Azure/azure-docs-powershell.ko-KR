---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/remove-azurermdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: 196d0eba5119ab984f9ffc632a301d3e65157f63
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702956"
---
# <span data-ttu-id="13286-101">Remove-AzureRmDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="13286-101">Remove-AzureRmDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="13286-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13286-102">SYNOPSIS</span></span>
<span data-ttu-id="13286-103">지정 된 Data Lake Store에서 지정 된 가상 네트워크 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="13286-103">Removes the specified virtual network rule in the specified Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="13286-104">구문과</span><span class="sxs-lookup"><span data-stu-id="13286-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreVirtualNetworkRule [-Account] <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13286-105">설명은</span><span class="sxs-lookup"><span data-stu-id="13286-105">DESCRIPTION</span></span>
<span data-ttu-id="13286-106">**AzureRmDataLakeStoreVirtualNetworkRule** cmdlet은 지정 된 Data Lake store에서 지정 된 가상 네트워크 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="13286-106">The **Remove-AzureRmDataLakeStoreVirtualNetworkRule** cmdlet removes the specified virtual network rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="13286-107">예제의</span><span class="sxs-lookup"><span data-stu-id="13286-107">EXAMPLES</span></span>

### <span data-ttu-id="13286-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="13286-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET"
```

<span data-ttu-id="13286-109">가상 네트워크 규칙 "myVNET"에서 계정 "dl"을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="13286-109">Removes virtual network rule "myVNET" from account "dls"</span></span>

## <span data-ttu-id="13286-110">변수</span><span class="sxs-lookup"><span data-stu-id="13286-110">PARAMETERS</span></span>

### <span data-ttu-id="13286-111">-계정</span><span class="sxs-lookup"><span data-stu-id="13286-111">-Account</span></span>
<span data-ttu-id="13286-112">의 가상 네트워크 규칙을 업데이트 하기 위한 Data Lake Store 계정</span><span class="sxs-lookup"><span data-stu-id="13286-112">The Data Lake Store account to update the virtual network rule in</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13286-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13286-113">-DefaultProfile</span></span>
<span data-ttu-id="13286-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="13286-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13286-115">-이름</span><span class="sxs-lookup"><span data-stu-id="13286-115">-Name</span></span>
<span data-ttu-id="13286-116">가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="13286-116">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13286-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="13286-117">-PassThru</span></span>
<span data-ttu-id="13286-118">삭제 작업의 결과를 표시 하는 부울 응답을 반환 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="13286-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13286-119">-확인</span><span class="sxs-lookup"><span data-stu-id="13286-119">-Confirm</span></span>
<span data-ttu-id="13286-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="13286-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13286-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13286-121">-WhatIf</span></span>
<span data-ttu-id="13286-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="13286-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13286-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="13286-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13286-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13286-124">CommonParameters</span></span>
<span data-ttu-id="13286-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="13286-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13286-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13286-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13286-127">입력</span><span class="sxs-lookup"><span data-stu-id="13286-127">INPUTS</span></span>

### <span data-ttu-id="13286-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="13286-128">System.String</span></span>

### <span data-ttu-id="13286-129">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="13286-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="13286-130">출력</span><span class="sxs-lookup"><span data-stu-id="13286-130">OUTPUTS</span></span>

### <span data-ttu-id="13286-131">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="13286-131">System.Boolean</span></span>

## <span data-ttu-id="13286-132">상속자</span><span class="sxs-lookup"><span data-stu-id="13286-132">NOTES</span></span>

## <span data-ttu-id="13286-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="13286-133">RELATED LINKS</span></span>
