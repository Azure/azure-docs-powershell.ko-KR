---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 66D543C0-34F0-47B1-943A-415DECF2155C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementGroup.md
ms.openlocfilehash: 058a82398be387913a0dd3eaf58c80ac12b692dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526403"
---
# <span data-ttu-id="e301b-101">Set-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="e301b-101">Set-AzureRmApiManagementGroup</span></span>

## <span data-ttu-id="e301b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e301b-102">SYNOPSIS</span></span>
<span data-ttu-id="e301b-103">API 관리 그룹을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="e301b-103">Configures an API management group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e301b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e301b-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementGroup -Context <PsApiManagementContext> -GroupId <String> [-Name <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e301b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e301b-105">DESCRIPTION</span></span>
<span data-ttu-id="e301b-106">**AzureRmApiManagementGroup** CMDLET은 API 관리 그룹을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="e301b-106">The **Set-AzureRmApiManagementGroup** cmdlet configures an API management group.</span></span>

## <span data-ttu-id="e301b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e301b-107">EXAMPLES</span></span>

### <span data-ttu-id="e301b-108">예제 1: 관리 그룹 구성</span><span class="sxs-lookup"><span data-stu-id="e301b-108">Example 1: Configure a management group</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementGroup -Context $apimContext -Description "Updated Management Group" -Name "Group0001"
```

<span data-ttu-id="e301b-109">이 명령은 Group0001 이라는 관리 그룹을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="e301b-109">This command configures a management group named Group0001.</span></span>

## <span data-ttu-id="e301b-110">변수</span><span class="sxs-lookup"><span data-stu-id="e301b-110">PARAMETERS</span></span>

### <span data-ttu-id="e301b-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="e301b-111">-Context</span></span>
<span data-ttu-id="e301b-112">**PsApiManagementContext** 개체의 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e301b-112">Specifies an instance of a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e301b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e301b-113">-DefaultProfile</span></span>
<span data-ttu-id="e301b-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e301b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e301b-115">-설명</span><span class="sxs-lookup"><span data-stu-id="e301b-115">-Description</span></span>
<span data-ttu-id="e301b-116">관리 그룹에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e301b-116">Specifies the description of the management group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e301b-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="e301b-117">-GroupId</span></span>
<span data-ttu-id="e301b-118">관리 그룹의 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e301b-118">Specifies the identifier of the management group.</span></span>

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

### <span data-ttu-id="e301b-119">-이름</span><span class="sxs-lookup"><span data-stu-id="e301b-119">-Name</span></span>
<span data-ttu-id="e301b-120">관리 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e301b-120">Specifies the name of the management group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e301b-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e301b-121">-PassThru</span></span>
<span data-ttu-id="e301b-122">passthru</span><span class="sxs-lookup"><span data-stu-id="e301b-122">passthru</span></span>

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

### <span data-ttu-id="e301b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e301b-123">CommonParameters</span></span>
<span data-ttu-id="e301b-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e301b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e301b-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e301b-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e301b-126">입력</span><span class="sxs-lookup"><span data-stu-id="e301b-126">INPUTS</span></span>

### <span data-ttu-id="e301b-127">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e301b-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e301b-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e301b-128">System.String</span></span>

### <span data-ttu-id="e301b-129">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="e301b-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e301b-130">출력</span><span class="sxs-lookup"><span data-stu-id="e301b-130">OUTPUTS</span></span>

### <span data-ttu-id="e301b-131">ApiManagement. ServiceManagement. \ PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="e301b-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="e301b-132">상속자</span><span class="sxs-lookup"><span data-stu-id="e301b-132">NOTES</span></span>

## <span data-ttu-id="e301b-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e301b-133">RELATED LINKS</span></span>

[<span data-ttu-id="e301b-134">Get-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="e301b-134">Get-AzureRmApiManagementGroup</span></span>](./Get-AzureRmApiManagementGroup.md)

[<span data-ttu-id="e301b-135">새로운 AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="e301b-135">New-AzureRmApiManagementGroup</span></span>](./New-AzureRmApiManagementGroup.md)

[<span data-ttu-id="e301b-136">제거-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="e301b-136">Remove-AzureRmApiManagementGroup</span></span>](./Remove-AzureRmApiManagementGroup.md)


