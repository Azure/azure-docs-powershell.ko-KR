---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppTrafficRouting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppTrafficRouting.md
ms.openlocfilehash: 0dda79130d150265d8050fcb5ba951cd243bebda
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056017"
---
# <span data-ttu-id="27250-101">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="27250-101">Remove-AzWebAppTrafficRouting</span></span>

## <span data-ttu-id="27250-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27250-102">SYNOPSIS</span></span>
<span data-ttu-id="27250-103">슬롯에서 라우팅 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="27250-103">Remove a routing Rule from the Slot.</span></span>

## <span data-ttu-id="27250-104">구문과</span><span class="sxs-lookup"><span data-stu-id="27250-104">SYNTAX</span></span>

```
Remove-AzWebAppTrafficRouting -ResourceGroupName <String> -WebAppName <String> -RuleName <String>
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27250-105">설명은</span><span class="sxs-lookup"><span data-stu-id="27250-105">DESCRIPTION</span></span>
<span data-ttu-id="27250-106">**AzWebAppTrafficRouting** Cmdlet은 Azure Web App 슬롯에서 라우팅 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="27250-106">The **Remove-AzWebAppTrafficRouting** cmdlet removes a routing rule from an Azure Web App Slot.</span></span>

## <span data-ttu-id="27250-107">예제의</span><span class="sxs-lookup"><span data-stu-id="27250-107">EXAMPLES</span></span>

### <span data-ttu-id="27250-108">예제 1 web app 슬롯에서 특정 라우팅 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="27250-108">Example 1 Removes the specific routing rule from webapp slot</span></span>
```powershell
PS C:\> Remove-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite"  -RuleName 'Stg'
```

<span data-ttu-id="27250-109">이 명령은 지정 된 web app 슬롯에 대 한 라우팅 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="27250-109">This command removes a routing rule for a given webapp slot.</span></span>

## <span data-ttu-id="27250-110">변수</span><span class="sxs-lookup"><span data-stu-id="27250-110">PARAMETERS</span></span>

### <span data-ttu-id="27250-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27250-111">-DefaultProfile</span></span>
<span data-ttu-id="27250-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="27250-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27250-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27250-113">-ResourceGroupName</span></span>
<span data-ttu-id="27250-114">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="27250-114">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27250-115">-RuleName</span><span class="sxs-lookup"><span data-stu-id="27250-115">-RuleName</span></span>
<span data-ttu-id="27250-116">규칙 이름</span><span class="sxs-lookup"><span data-stu-id="27250-116">Rule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27250-117">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="27250-117">-WebAppName</span></span>
<span data-ttu-id="27250-118">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="27250-118">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27250-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="27250-119">-PassThru</span></span>
<span data-ttu-id="27250-120">액세스 제한 구성 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="27250-120">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="27250-121">-확인</span><span class="sxs-lookup"><span data-stu-id="27250-121">-Confirm</span></span>
<span data-ttu-id="27250-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="27250-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27250-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27250-123">-WhatIf</span></span>
<span data-ttu-id="27250-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="27250-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27250-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="27250-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27250-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27250-126">CommonParameters</span></span>
<span data-ttu-id="27250-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="27250-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27250-128">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="27250-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27250-129">입력</span><span class="sxs-lookup"><span data-stu-id="27250-129">INPUTS</span></span>

### <span data-ttu-id="27250-130">않아야</span><span class="sxs-lookup"><span data-stu-id="27250-130">None</span></span>

## <span data-ttu-id="27250-131">출력</span><span class="sxs-lookup"><span data-stu-id="27250-131">OUTPUTS</span></span>

### <span data-ttu-id="27250-132">RampUpRule/. m i.</span><span class="sxs-lookup"><span data-stu-id="27250-132">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span></span>

## <span data-ttu-id="27250-133">상속자</span><span class="sxs-lookup"><span data-stu-id="27250-133">NOTES</span></span>

## <span data-ttu-id="27250-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="27250-134">RELATED LINKS</span></span>
[<span data-ttu-id="27250-135">추가-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="27250-135">Add-AzWebAppTrafficRouting</span></span>](./Add-AzWebAppTrafficRouting.md)

[<span data-ttu-id="27250-136">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="27250-136">Get-AzWebAppTrafficRouting</span></span>](./Get-AzWebAppTrafficRouting.md)

[<span data-ttu-id="27250-137">업데이트-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="27250-137">Update-AzWebAppTrafficRouting</span></span>](./Update-AzWebAppTrafficRouting.md)