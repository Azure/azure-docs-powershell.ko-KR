---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/remove-azurermanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Remove-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Remove-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 4976c34437b2f858f8e76924754fe04a8b1e0a84
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531522"
---
# <span data-ttu-id="faf79-101">Remove-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="faf79-101">Remove-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="faf79-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="faf79-102">SYNOPSIS</span></span>
<span data-ttu-id="faf79-103">Analysis Services 서버 인스턴스 삭제</span><span class="sxs-lookup"><span data-stu-id="faf79-103">Deletes an instance of Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="faf79-104">구문과</span><span class="sxs-lookup"><span data-stu-id="faf79-104">SYNTAX</span></span>

```
Remove-AzureRmAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="faf79-105">설명은</span><span class="sxs-lookup"><span data-stu-id="faf79-105">DESCRIPTION</span></span>
<span data-ttu-id="faf79-106">Remove-AzureRmAnalysisServicesServer cmdlet은 Analysis Services 서버의 인스턴스를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="faf79-106">The Remove-AzureRmAnalysisServicesServer cmdlet  deletes an instance of Analysis Services server</span></span>

## <span data-ttu-id="faf79-107">예제의</span><span class="sxs-lookup"><span data-stu-id="faf79-107">EXAMPLES</span></span>

### <span data-ttu-id="faf79-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="faf79-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="faf79-109">이 명령은 resourcegroup testserver에서 testserver 라는 서버를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="faf79-109">This command will remove the server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="faf79-110">변수</span><span class="sxs-lookup"><span data-stu-id="faf79-110">PARAMETERS</span></span>

### <span data-ttu-id="faf79-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="faf79-111">-DefaultProfile</span></span>
<span data-ttu-id="faf79-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="faf79-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="faf79-113">-이름</span><span class="sxs-lookup"><span data-stu-id="faf79-113">-Name</span></span>
<span data-ttu-id="faf79-114">Analysis Services 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="faf79-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="faf79-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="faf79-115">-PassThru</span></span>
<span data-ttu-id="faf79-116">작업이 성공적으로 완료 되 면 삭제 된 서버 세부 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="faf79-116">Will return the deleted server details if the operation completes successfully</span></span>

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

### <span data-ttu-id="faf79-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="faf79-117">-ResourceGroupName</span></span>
<span data-ttu-id="faf79-118">서버가 속한 Azure 리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="faf79-118">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="faf79-119">-확인</span><span class="sxs-lookup"><span data-stu-id="faf79-119">-Confirm</span></span>
<span data-ttu-id="faf79-120">사용자에 게 작업 수행 여부 확인 메시지 표시</span><span class="sxs-lookup"><span data-stu-id="faf79-120">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="faf79-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="faf79-121">-WhatIf</span></span>
<span data-ttu-id="faf79-122">현재 작업이 실제로 수행 하지 않고 수행 하는 작업에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="faf79-122">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="faf79-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="faf79-123">CommonParameters</span></span>
<span data-ttu-id="faf79-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="faf79-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="faf79-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="faf79-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="faf79-126">입력</span><span class="sxs-lookup"><span data-stu-id="faf79-126">INPUTS</span></span>

### <span data-ttu-id="faf79-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="faf79-127">System.String</span></span>

## <span data-ttu-id="faf79-128">출력</span><span class="sxs-lookup"><span data-stu-id="faf79-128">OUTPUTS</span></span>

### <span data-ttu-id="faf79-129">AnalysisServices. AzureAnalysisServicesServer/.</span><span class="sxs-lookup"><span data-stu-id="faf79-129">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="faf79-130">상속자</span><span class="sxs-lookup"><span data-stu-id="faf79-130">NOTES</span></span>
<span data-ttu-id="faf79-131">별칭: Remove-AzureAs</span><span class="sxs-lookup"><span data-stu-id="faf79-131">Alias: Remove-AzureAs</span></span>

## <span data-ttu-id="faf79-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="faf79-132">RELATED LINKS</span></span>

[<span data-ttu-id="faf79-133">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="faf79-133">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="faf79-134">새로운 AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="faf79-134">New-AzureRmAnalysisServicesServer</span></span>](./New-AzureRmAnalysisServicesServer.md)
