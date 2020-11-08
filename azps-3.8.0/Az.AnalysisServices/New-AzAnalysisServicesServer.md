---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/new-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesServer.md
ms.openlocfilehash: 7e6b41a081b5170a34863ff29bf26431224490fc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94041972"
---
# <span data-ttu-id="60af7-101">New-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="60af7-101">New-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="60af7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60af7-102">SYNOPSIS</span></span>
<span data-ttu-id="60af7-103">새 Analysis Services 서버를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="60af7-103">Creates a new Analysis Services server</span></span>

## <span data-ttu-id="60af7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="60af7-104">SYNTAX</span></span>

```
New-AzAnalysisServicesServer [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Sku] <String> [[-Tag] <Hashtable>] [[-Administrator] <String>] [[-BackupBlobContainerUri] <String>]
 [-ReadonlyReplicaCount <Int32>] [-DefaultConnectionMode <String>]
 [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>] [-GatewayResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60af7-105">설명은</span><span class="sxs-lookup"><span data-stu-id="60af7-105">DESCRIPTION</span></span>
<span data-ttu-id="60af7-106">New-AzAnalysisServicesServer cmdlet은 새 Analysis Services 서버를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="60af7-106">The New-AzAnalysisServicesServer cmdlet creates a new Analysis Services server</span></span>

## <span data-ttu-id="60af7-107">예제의</span><span class="sxs-lookup"><span data-stu-id="60af7-107">EXAMPLES</span></span>

### <span data-ttu-id="60af7-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="60af7-108">Example 1</span></span>
```
PS C:\> New-AzAnalysisServicesServer -ResourceGroupName "testresourcegroup" -Name "testserver" -Location "West-US" -Sku "S1"
```

<span data-ttu-id="60af7-109">Azure 지역 서 비 US와 리소스 그룹 testserver에 testserver 라는 서버를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="60af7-109">Creates a server named testserver in the Azure region West-US and in resource group testresourcegroup.</span></span> <span data-ttu-id="60af7-110">서버에 대 한 sku 수준은 S1이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="60af7-110">The sku level for the server will be S1.</span></span>

## <span data-ttu-id="60af7-111">변수</span><span class="sxs-lookup"><span data-stu-id="60af7-111">PARAMETERS</span></span>

### <span data-ttu-id="60af7-112">-관리자</span><span class="sxs-lookup"><span data-stu-id="60af7-112">-Administrator</span></span>
<span data-ttu-id="60af7-113">서버의 관리자로 설정할 사용자 또는 그룹의 쉼표로 구분 된 목록을 나타내는 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="60af7-113">A string representing a comma separated list of users or groups to be set as administrators on the server.</span></span> <span data-ttu-id="60af7-114">사용자 또는 그룹에 UPN 형식 (예: 또는)을 지정 해야 합니다. user@contoso.comgroups@contoso.com</span><span class="sxs-lookup"><span data-stu-id="60af7-114">The users or groups need to be specified UPN format e.g. user@contoso.com or groups@contoso.com</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60af7-115">-BackupBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="60af7-115">-BackupBlobContainerUri</span></span>
<span data-ttu-id="60af7-116">Analysis Services 서버 백업용 blob 컨테이너 Uri</span><span class="sxs-lookup"><span data-stu-id="60af7-116">The blob container Uri for backup the Analysis Services server</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60af7-117">-DefaultConnectionMode</span><span class="sxs-lookup"><span data-stu-id="60af7-117">-DefaultConnectionMode</span></span>
<span data-ttu-id="60af7-118">Analysis service 서버의 기본 연결 모드</span><span class="sxs-lookup"><span data-stu-id="60af7-118">Default connection mode of an Analysis service server</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: All, Readonly

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60af7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60af7-119">-DefaultProfile</span></span>
<span data-ttu-id="60af7-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="60af7-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60af7-121">-FirewallConfig</span><span class="sxs-lookup"><span data-stu-id="60af7-121">-FirewallConfig</span></span>
<span data-ttu-id="60af7-122">분석 서버의 방화벽 구성</span><span class="sxs-lookup"><span data-stu-id="60af7-122">Firewall config of an Analysis server</span></span>

```yaml
Type: Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60af7-123">-게이트웨이 Resourceid</span><span class="sxs-lookup"><span data-stu-id="60af7-123">-GatewayResourceId</span></span>
<span data-ttu-id="60af7-124">분석 서버에 연결 하는 게이트웨이 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="60af7-124">Gateway resource Id to associate to an Analysis server</span></span>

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

### <span data-ttu-id="60af7-125">-위치</span><span class="sxs-lookup"><span data-stu-id="60af7-125">-Location</span></span>
<span data-ttu-id="60af7-126">Analysis Services 서버가 호스팅되는 Azure 지역입니다.</span><span class="sxs-lookup"><span data-stu-id="60af7-126">The Azure region where the Analysis Services server is hosted</span></span>

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

### <span data-ttu-id="60af7-127">-이름</span><span class="sxs-lookup"><span data-stu-id="60af7-127">-Name</span></span>
<span data-ttu-id="60af7-128">Analysis Services 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="60af7-128">Name of the Analysis Services server</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60af7-129">-ReadonlyReplicaCount</span><span class="sxs-lookup"><span data-stu-id="60af7-129">-ReadonlyReplicaCount</span></span>
<span data-ttu-id="60af7-130">분석 서비스 서버의 복제 횟수 읽기</span><span class="sxs-lookup"><span data-stu-id="60af7-130">Read only replica count of an Analysis service server</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60af7-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60af7-131">-ResourceGroupName</span></span>
<span data-ttu-id="60af7-132">서버가 속한 Azure 리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="60af7-132">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="60af7-133">-Sku</span><span class="sxs-lookup"><span data-stu-id="60af7-133">-Sku</span></span>
<span data-ttu-id="60af7-134">서버의 Sku 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="60af7-134">The name of the Sku for the server.</span></span>
<span data-ttu-id="60af7-135">지원 되는 값은 표준 계층에 대 한 0 ', ' 1 ', ' 2 ', 4 '입니다. 기본 계층에 대 한 ' B1 ', ' B2 ', 개발 계층의 경우 1 '입니다.</span><span class="sxs-lookup"><span data-stu-id="60af7-135">The supported values are 'S0', 'S1', 'S2', 'S4' for the Standard tier; 'B1', 'B2' for the Basic tier and 'D1' for Development tier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60af7-136">태그</span><span class="sxs-lookup"><span data-stu-id="60af7-136">-Tag</span></span>
<span data-ttu-id="60af7-137">서버에서 태그로 설정 된 해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="60af7-137">Key-value pairs in the form of a hash table set as tags on the server.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60af7-138">-확인</span><span class="sxs-lookup"><span data-stu-id="60af7-138">-Confirm</span></span>
<span data-ttu-id="60af7-139">사용자에 게 작업 수행 여부 확인 메시지 표시</span><span class="sxs-lookup"><span data-stu-id="60af7-139">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="60af7-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60af7-140">-WhatIf</span></span>
<span data-ttu-id="60af7-141">현재 작업이 실제로 수행 하지 않고 수행 하는 작업에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="60af7-141">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="60af7-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60af7-142">CommonParameters</span></span>
<span data-ttu-id="60af7-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="60af7-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60af7-144">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60af7-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60af7-145">입력</span><span class="sxs-lookup"><span data-stu-id="60af7-145">INPUTS</span></span>

### <span data-ttu-id="60af7-146">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="60af7-146">System.String</span></span>

### <span data-ttu-id="60af7-147">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="60af7-147">System.Collections.Hashtable</span></span>

### <span data-ttu-id="60af7-148">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="60af7-148">System.Int32</span></span>

### <span data-ttu-id="60af7-149">AnalysisServices. PsAzureAnalysisServicesFirewallConfig/.</span><span class="sxs-lookup"><span data-stu-id="60af7-149">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="60af7-150">출력</span><span class="sxs-lookup"><span data-stu-id="60af7-150">OUTPUTS</span></span>

### <span data-ttu-id="60af7-151">AnalysisServices. AzureAnalysisServicesServer/.</span><span class="sxs-lookup"><span data-stu-id="60af7-151">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="60af7-152">상속자</span><span class="sxs-lookup"><span data-stu-id="60af7-152">NOTES</span></span>
<span data-ttu-id="60af7-153">별칭: New-AzAs</span><span class="sxs-lookup"><span data-stu-id="60af7-153">Alias: New-AzAs</span></span>

## <span data-ttu-id="60af7-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="60af7-154">RELATED LINKS</span></span>

[<span data-ttu-id="60af7-155">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="60af7-155">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="60af7-156">제거-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="60af7-156">Remove-AzAnalysisServicesServer</span></span>](./Remove-AzAnalysisServicesServer.md)
