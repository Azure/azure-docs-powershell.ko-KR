---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 6C7A7E1A-87A2-4F0D-9091-413C111F47F0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/remove-azurermdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreFirewallRule.md
ms.openlocfilehash: 7e762ed090b0076c5cc8d0b359cf8883ae26265d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524459"
---
# <span data-ttu-id="87384-101">Remove-AzureRmDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="87384-101">Remove-AzureRmDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="87384-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87384-102">SYNOPSIS</span></span>
<span data-ttu-id="87384-103">지정 된 Data Lake Store에서 지정 된 방화벽 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="87384-103">Removes the specified firewall rule in the specified Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87384-104">구문과</span><span class="sxs-lookup"><span data-stu-id="87384-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreFirewallRule [-Account] <String> [[-Name] <String>] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="87384-105">설명은</span><span class="sxs-lookup"><span data-stu-id="87384-105">DESCRIPTION</span></span>
<span data-ttu-id="87384-106">**AzureRmDataLakeStoreFirewallRule** cmdlet은 지정 된 Data Lake store에서 지정 된 방화벽 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="87384-106">The **Remove-AzureRmDataLakeStoreFirewallRule** cmdlet removes the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="87384-107">예제의</span><span class="sxs-lookup"><span data-stu-id="87384-107">EXAMPLES</span></span>

### <span data-ttu-id="87384-108">예제 1: 계정에서 방화벽 규칙 제거</span><span class="sxs-lookup"><span data-stu-id="87384-108">Example 1: Remove a firewall rule from an account</span></span>
```
PS C:\> Remove-AzureRmDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule
```

<span data-ttu-id="87384-109">"ContosoADL" 계정에서 "MyFirewallRule" 방화벽 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="87384-109">Removes firewall rule "MyFirewallRule" from account "ContosoADL"</span></span>

## <span data-ttu-id="87384-110">변수</span><span class="sxs-lookup"><span data-stu-id="87384-110">PARAMETERS</span></span>

### <span data-ttu-id="87384-111">-계정</span><span class="sxs-lookup"><span data-stu-id="87384-111">-Account</span></span>
<span data-ttu-id="87384-112">방화벽 규칙을 업데이트 하기 위한 Data Lake Store 계정</span><span class="sxs-lookup"><span data-stu-id="87384-112">The Data Lake Store account to update the firewall rule in</span></span>

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

### <span data-ttu-id="87384-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87384-113">-DefaultProfile</span></span>
<span data-ttu-id="87384-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="87384-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="87384-115">-이름</span><span class="sxs-lookup"><span data-stu-id="87384-115">-Name</span></span>
<span data-ttu-id="87384-116">삭제할 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="87384-116">The name of the firewall rule to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87384-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="87384-117">-PassThru</span></span>
<span data-ttu-id="87384-118">삭제 작업의 결과를 표시 하는 부울 응답을 반환 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="87384-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87384-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87384-119">-ResourceGroupName</span></span>
<span data-ttu-id="87384-120">방화벽 규칙을 제거할 계정이 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="87384-120">Specifies the name of the resource group that contains the account to remove the firewall rule from.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87384-121">-확인</span><span class="sxs-lookup"><span data-stu-id="87384-121">-Confirm</span></span>
<span data-ttu-id="87384-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="87384-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87384-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87384-123">-WhatIf</span></span>
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

### <span data-ttu-id="87384-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87384-124">CommonParameters</span></span>
<span data-ttu-id="87384-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="87384-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87384-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87384-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87384-127">입력</span><span class="sxs-lookup"><span data-stu-id="87384-127">INPUTS</span></span>

### <span data-ttu-id="87384-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="87384-128">System.String</span></span>

### <span data-ttu-id="87384-129">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="87384-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="87384-130">출력</span><span class="sxs-lookup"><span data-stu-id="87384-130">OUTPUTS</span></span>

### <span data-ttu-id="87384-131">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="87384-131">System.Boolean</span></span>

## <span data-ttu-id="87384-132">상속자</span><span class="sxs-lookup"><span data-stu-id="87384-132">NOTES</span></span>

## <span data-ttu-id="87384-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="87384-133">RELATED LINKS</span></span>
