---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/set-azurermanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Set-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Set-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 485687b0a08ca69edc77b4ee5f9510ad8a1396a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528163"
---
# <span data-ttu-id="117f7-101">Set-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="117f7-101">Set-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="117f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="117f7-102">SYNOPSIS</span></span>
<span data-ttu-id="117f7-103">Analysis Services 서버 인스턴스 수정</span><span class="sxs-lookup"><span data-stu-id="117f7-103">Modifies  an instance of Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="117f7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="117f7-104">SYNTAX</span></span>

### <span data-ttu-id="117f7-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="117f7-105">Default (Default)</span></span>
```
Set-AzureRmAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [[-BackupBlobContainerUri] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="117f7-106">DisableBackup</span><span class="sxs-lookup"><span data-stu-id="117f7-106">DisableBackup</span></span>
```
Set-AzureRmAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [[-Sku] <String>]
 [[-Tag] <Hashtable>] [[-Administrator] <String>] [-PassThru] [-DisableBackup]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="117f7-107">설명은</span><span class="sxs-lookup"><span data-stu-id="117f7-107">DESCRIPTION</span></span>
<span data-ttu-id="117f7-108">Set-AzureRmAnalysisServicesServer cmdlet은 Analysis Services 서버의 인스턴스를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="117f7-108">The Set-AzureRmAnalysisServicesServer cmdlet modifies an instance of Analysis Services server</span></span>

## <span data-ttu-id="117f7-109">예제의</span><span class="sxs-lookup"><span data-stu-id="117f7-109">EXAMPLES</span></span>

### <span data-ttu-id="117f7-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="117f7-110">Example 1</span></span>
```
PS C:\> Set-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup" -Tag "key1:value1,key2:value2" -Administrator "testuser1@contoso.com"
```

<span data-ttu-id="117f7-111">Resourcegroup에 대 한 testserver 라는 서버를 수정 하 여 태그를 key1로 설정 합니다. value1 및 key2: value2 및 관리자가 testuser1@contoso.com</span><span class="sxs-lookup"><span data-stu-id="117f7-111">Modifies the server named testserver in resourcegroup testgroup to set the tags as key1:value1 and key2:value2 and administrator to testuser1@contoso.com</span></span>

## <span data-ttu-id="117f7-112">변수</span><span class="sxs-lookup"><span data-stu-id="117f7-112">PARAMETERS</span></span>

### <span data-ttu-id="117f7-113">-관리자</span><span class="sxs-lookup"><span data-stu-id="117f7-113">-Administrator</span></span>
<span data-ttu-id="117f7-114">서버의 관리자로 설정할 사용자 또는 그룹의 쉼표로 구분 된 목록을 나타내는 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="117f7-114">A string representing a comma separated list of users or groups to be set as administrators on the server.</span></span>
<span data-ttu-id="117f7-115">사용자 또는 그룹에 UPN 형식 (예: 또는)을 지정 해야 합니다. user@contoso.comgroups@contoso.com</span><span class="sxs-lookup"><span data-stu-id="117f7-115">The users or groups need to be specified UPN format e.g. user@contoso.com or groups@contoso.com</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="117f7-116">-BackupBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="117f7-116">-BackupBlobContainerUri</span></span>
<span data-ttu-id="117f7-117">Analysis Services 서버 백업용 blob 컨테이너 Uri</span><span class="sxs-lookup"><span data-stu-id="117f7-117">The blob container Uri for backup the Analysis Services server</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="117f7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="117f7-118">-DefaultProfile</span></span>
<span data-ttu-id="117f7-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="117f7-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="117f7-120">-DisableBackup</span><span class="sxs-lookup"><span data-stu-id="117f7-120">-DisableBackup</span></span>
<span data-ttu-id="117f7-121">백업 blob 컨테이너를 사용 하지 않도록 전환 합니다.</span><span class="sxs-lookup"><span data-stu-id="117f7-121">The switch to disable backup blob container.</span></span>
<span data-ttu-id="117f7-122">백업 blob 컨테이너를 다시 사용 하도록 설정 하려면 백업 blob 컨테이너 Uri를-BackupBlobContainerUri로 제공 하세요.</span><span class="sxs-lookup"><span data-stu-id="117f7-122">To re-enable the backup blob container, please provide the backup blob container Uri as -BackupBlobContainerUri.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DisableBackup
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="117f7-123">-이름</span><span class="sxs-lookup"><span data-stu-id="117f7-123">-Name</span></span>
<span data-ttu-id="117f7-124">Analysis Services 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="117f7-124">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="117f7-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="117f7-125">-PassThru</span></span>
<span data-ttu-id="117f7-126">작업이 성공적으로 완료 되 면 삭제 된 서버 세부 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="117f7-126">Will return the deleted server details if the operation completes successfully</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="117f7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="117f7-127">-ResourceGroupName</span></span>
<span data-ttu-id="117f7-128">서버가 속한 Azure 리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="117f7-128">Name of the Azure resource group to which the server belongs</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="117f7-129">-Sku</span><span class="sxs-lookup"><span data-stu-id="117f7-129">-Sku</span></span>
<span data-ttu-id="117f7-130">서버의 Sku 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="117f7-130">The name of the Sku for the server.</span></span>
<span data-ttu-id="117f7-131">지원 되는 값은 표준 계층에 대 한 0 ', ' 1 ', ' 2 ', 4 '입니다. 기본 계층에 대 한 ' B1 ', ' B2 ', 개발 계층의 경우 1 '입니다.</span><span class="sxs-lookup"><span data-stu-id="117f7-131">The supported values are 'S0', 'S1', 'S2', 'S4' for the Standard tier; 'B1', 'B2' for the Basic tier and 'D1' for Development tier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="117f7-132">태그</span><span class="sxs-lookup"><span data-stu-id="117f7-132">-Tag</span></span>
<span data-ttu-id="117f7-133">서버에서 태그로 설정 된 해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="117f7-133">Key-value pairs in the form of a hash table set as tags on the server.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="117f7-134">-ReadonlyReplicaCount</span><span class="sxs-lookup"><span data-stu-id="117f7-134">-ReadonlyReplicaCount</span></span>
<span data-ttu-id="117f7-135">분석 서비스 서버의 복제 횟수 읽기</span><span class="sxs-lookup"><span data-stu-id="117f7-135">Read only replica count of an Analysis service server</span></span>

```yaml
Type: Integer
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="117f7-136">-DefaultConnectionMode</span><span class="sxs-lookup"><span data-stu-id="117f7-136">-DefaultConnectionMode</span></span>
<span data-ttu-id="117f7-137">Analysis service 서버의 기본 연결 모드</span><span class="sxs-lookup"><span data-stu-id="117f7-137">Default connection mode of an Analysis service server</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="117f7-138">-FirewallConfig</span><span class="sxs-lookup"><span data-stu-id="117f7-138">-FirewallConfig</span></span>
<span data-ttu-id="117f7-139">분석 서버의 방화벽 구성</span><span class="sxs-lookup"><span data-stu-id="117f7-139">Firewall config of an Analysis server</span></span>

```yaml
Type: Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesFirewallConfig
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="117f7-140">-확인</span><span class="sxs-lookup"><span data-stu-id="117f7-140">-Confirm</span></span>
<span data-ttu-id="117f7-141">사용자에 게 작업 수행 여부 확인 메시지 표시</span><span class="sxs-lookup"><span data-stu-id="117f7-141">Prompts user to confirm whether to perform the operation</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="117f7-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="117f7-142">-WhatIf</span></span>
<span data-ttu-id="117f7-143">현재 작업이 실제로 수행 하지 않고 수행 하는 작업에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="117f7-143">Describes the actions the current operation will perform without actually performing them</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="117f7-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="117f7-144">CommonParameters</span></span>
<span data-ttu-id="117f7-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="117f7-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="117f7-146">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="117f7-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="117f7-147">입력</span><span class="sxs-lookup"><span data-stu-id="117f7-147">INPUTS</span></span>

### <span data-ttu-id="117f7-148">않아야</span><span class="sxs-lookup"><span data-stu-id="117f7-148">None</span></span>
<span data-ttu-id="117f7-149">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="117f7-149">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="117f7-150">출력</span><span class="sxs-lookup"><span data-stu-id="117f7-150">OUTPUTS</span></span>

### <span data-ttu-id="117f7-151">AnalysisServicesServer를 통한 분석.</span><span class="sxs-lookup"><span data-stu-id="117f7-151">Microsoft.Azure.Management.Analysis.Models.AnalysisServicesServer</span></span>

## <span data-ttu-id="117f7-152">상속자</span><span class="sxs-lookup"><span data-stu-id="117f7-152">NOTES</span></span>
<span data-ttu-id="117f7-153">별칭: Set-AzureAs</span><span class="sxs-lookup"><span data-stu-id="117f7-153">Alias: Set-AzureAs</span></span>

## <span data-ttu-id="117f7-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="117f7-154">RELATED LINKS</span></span>

[<span data-ttu-id="117f7-155">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="117f7-155">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="117f7-156">제거-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="117f7-156">Remove-AzureRmAnalysisServicesServer</span></span>](./Remove-AzureRmAnalysisServicesServer.md)
