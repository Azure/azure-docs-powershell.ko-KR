---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/powershell/module/az.analysisservices/get-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Get-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Get-AzAnalysisServicesServer.md
ms.openlocfilehash: 8c2e7b9fe5335df29308a612ef8a133762e7ab4c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015536"
---
# <span data-ttu-id="8a0be-101">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="8a0be-101">Get-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="8a0be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a0be-102">SYNOPSIS</span></span>
<span data-ttu-id="8a0be-103">Analysis Services 서버의 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8a0be-103">Gets the details of an Analysis Services server.</span></span>

## <span data-ttu-id="8a0be-104">구문</span><span class="sxs-lookup"><span data-stu-id="8a0be-104">SYNTAX</span></span>

```
Get-AzAnalysisServicesServer [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8a0be-105">설명</span><span class="sxs-lookup"><span data-stu-id="8a0be-105">DESCRIPTION</span></span>
<span data-ttu-id="8a0be-106">Get-AzAnalysisServicesServer cmdlet은 Analysis Services 서버의 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8a0be-106">The Get-AzAnalysisServicesServer cmdlet gets the details of an Analysis Services server.</span></span>

## <span data-ttu-id="8a0be-107">예제</span><span class="sxs-lookup"><span data-stu-id="8a0be-107">EXAMPLES</span></span>

### <span data-ttu-id="8a0be-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="8a0be-108">Example 1</span></span>
```
PS C:\>Get-AzAnalysisServicesServer -ResourceGroupName "ResourceGroup03"
```

<span data-ttu-id="8a0be-109">이 명령은 ResourceGroup03이라는 리소스 그룹의 모든 Azure Analysis Services 서버를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8a0be-109">This command gets all Azure Analysis Services servers in the resource group named ResourceGroup03.</span></span>

### <span data-ttu-id="8a0be-110">예제 2: 서버 얻기</span><span class="sxs-lookup"><span data-stu-id="8a0be-110">Example 2: Get a server</span></span>
```
PS C:\>Get-AzAnalysisServicesServer -ResourceGroupName "ResourceGroup03" -Name "testserver"
```

<span data-ttu-id="8a0be-111">이 명령은 ResourceGroup03이라는 리소스 그룹에서 Testserver라는 Azure Analysis Services 서버를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8a0be-111">This command gets the Azure Analysis Services server named testserver in the resource group named ResourceGroup03.</span></span>

## <span data-ttu-id="8a0be-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="8a0be-112">PARAMETERS</span></span>

### <span data-ttu-id="8a0be-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a0be-113">-DefaultProfile</span></span>
<span data-ttu-id="8a0be-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8a0be-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a0be-115">-Name</span><span class="sxs-lookup"><span data-stu-id="8a0be-115">-Name</span></span>
<span data-ttu-id="8a0be-116">Analysis Services 서버 이름</span><span class="sxs-lookup"><span data-stu-id="8a0be-116">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="8a0be-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a0be-117">-ResourceGroupName</span></span>
<span data-ttu-id="8a0be-118">서버가 속한 Azure 리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="8a0be-118">Name of the Azure resource group to which the server belongs</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a0be-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a0be-119">CommonParameters</span></span>
<span data-ttu-id="8a0be-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8a0be-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a0be-121">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="8a0be-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a0be-122">입력</span><span class="sxs-lookup"><span data-stu-id="8a0be-122">INPUTS</span></span>

### <span data-ttu-id="8a0be-123">System.String</span><span class="sxs-lookup"><span data-stu-id="8a0be-123">System.String</span></span>

## <span data-ttu-id="8a0be-124">출력</span><span class="sxs-lookup"><span data-stu-id="8a0be-124">OUTPUTS</span></span>

### <span data-ttu-id="8a0be-125">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="8a0be-125">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="8a0be-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8a0be-126">NOTES</span></span>
<span data-ttu-id="8a0be-127">별칭: Get-AzAs</span><span class="sxs-lookup"><span data-stu-id="8a0be-127">Alias: Get-AzAs</span></span>

## <span data-ttu-id="8a0be-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8a0be-128">RELATED LINKS</span></span>

[<span data-ttu-id="8a0be-129">New-AzAnalysisServicesServer </span><span class="sxs-lookup"><span data-stu-id="8a0be-129">New-AzAnalysisServicesServer </span></span>](./New-AzAnalysisServicesServer .md)

[<span data-ttu-id="8a0be-130">Remove-AzAnalysisServicesServer </span><span class="sxs-lookup"><span data-stu-id="8a0be-130">Remove-AzAnalysisServicesServer </span></span>](./Remove-AzAnalysisServicesServer .md)
