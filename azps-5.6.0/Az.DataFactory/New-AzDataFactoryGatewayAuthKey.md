---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/new-azdatafactorygatewayauthkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryGatewayAuthKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryGatewayAuthKey.md
ms.openlocfilehash: e58df40aa227e1c8132902c467c2dbcb881c7b6f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974960"
---
# <span data-ttu-id="26c0e-101">New-AzDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="26c0e-101">New-AzDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="26c0e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26c0e-102">SYNOPSIS</span></span>
<span data-ttu-id="26c0e-103">Azure Data Factory Gateway에 대한 공인 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="26c0e-103">Creates auth key for an Azure Data Factory Gateway.</span></span>

## <span data-ttu-id="26c0e-104">구문</span><span class="sxs-lookup"><span data-stu-id="26c0e-104">SYNTAX</span></span>

### <span data-ttu-id="26c0e-105">ByFactoryName(기본값)</span><span class="sxs-lookup"><span data-stu-id="26c0e-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryGatewayAuthKey [-DataFactoryName] <String> [-GatewayName] <String> [-KeyName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="26c0e-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="26c0e-106">ByFactoryObject</span></span>
```
New-AzDataFactoryGatewayAuthKey [-InputObject] <PSDataFactory> [-GatewayName] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26c0e-107">설명</span><span class="sxs-lookup"><span data-stu-id="26c0e-107">DESCRIPTION</span></span>
<span data-ttu-id="26c0e-108">**New-AzDataFactoryGatewayAuthKey** cmdlet은 지정된 Azure Data Factory 게이트웨이에 대한 게이트웨이 Auth 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="26c0e-108">The **New-AzDataFactoryGatewayAuthKey** cmdlet creates gateway auth key for a specified Azure Data Factory gateway.</span></span>
<span data-ttu-id="26c0e-109">이 키를 사용하여 클라우드 서비스에 게이트웨이를 등록합니다.</span><span class="sxs-lookup"><span data-stu-id="26c0e-109">You register the gateway with a cloud service by using this key.</span></span>

## <span data-ttu-id="26c0e-110">예제</span><span class="sxs-lookup"><span data-stu-id="26c0e-110">EXAMPLES</span></span>

### <span data-ttu-id="26c0e-111">예제 1: Key1에 대한 게이트웨이 공개 키 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="26c0e-111">Example 1: Creates a gateway auth key for Key1</span></span>
```
PS C:\> New-AzDataFactoryGatewayAuthKey -ResourceGroup ADFResource -GatewayName 'MyGateway' -DataFactoryName MyADF -KeyName key1
Key1 : DMG@632e739e-1053-4070-9102-8591f067526e@41fcbc45-c594-4152-a8f1-fcbcd6452aea@wu@BH0EV9hu/o2IYGQzfYYD203XhdS6Tty
       fkYwYFbG6wBU=
Key2 :
```

<span data-ttu-id="26c0e-112">이 명령은 MyGateway라는 데이터 팩터리 게이트웨이에 대한 Key1의 게이트웨이 공개 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="26c0e-112">This command creates a gateway auth key of Key1 for the data factory gateway named MyGateway.</span></span>

## <span data-ttu-id="26c0e-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="26c0e-113">PARAMETERS</span></span>

### <span data-ttu-id="26c0e-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="26c0e-114">-DataFactoryName</span></span>
<span data-ttu-id="26c0e-115">데이터 팩터리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="26c0e-115">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26c0e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26c0e-116">-DefaultProfile</span></span>
<span data-ttu-id="26c0e-117">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="26c0e-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="26c0e-118">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="26c0e-118">-GatewayName</span></span>
<span data-ttu-id="26c0e-119">데이터 팩터리 게이트웨이 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="26c0e-119">The data factory gateway name.</span></span>

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

### <span data-ttu-id="26c0e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="26c0e-120">-InputObject</span></span>
<span data-ttu-id="26c0e-121">데이터 팩터리 개체</span><span class="sxs-lookup"><span data-stu-id="26c0e-121">The data factory object</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: DataFactory

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="26c0e-122">-KeyName</span><span class="sxs-lookup"><span data-stu-id="26c0e-122">-KeyName</span></span>
<span data-ttu-id="26c0e-123">다시 생성될 게이트웨이 공개 키의 이름('key1' 또는 'key2').</span><span class="sxs-lookup"><span data-stu-id="26c0e-123">The name of gateway auth key to be regenerated, either 'key1' or 'key2'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: key1, key2

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26c0e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26c0e-124">-ResourceGroupName</span></span>
<span data-ttu-id="26c0e-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="26c0e-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26c0e-126">-확인</span><span class="sxs-lookup"><span data-stu-id="26c0e-126">-Confirm</span></span>
<span data-ttu-id="26c0e-127">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="26c0e-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26c0e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26c0e-128">-WhatIf</span></span>
<span data-ttu-id="26c0e-129">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="26c0e-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="26c0e-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="26c0e-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26c0e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26c0e-131">CommonParameters</span></span>
<span data-ttu-id="26c0e-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="26c0e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26c0e-133">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="26c0e-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26c0e-134">입력</span><span class="sxs-lookup"><span data-stu-id="26c0e-134">INPUTS</span></span>

### <span data-ttu-id="26c0e-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="26c0e-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="26c0e-136">System.String</span><span class="sxs-lookup"><span data-stu-id="26c0e-136">System.String</span></span>

## <span data-ttu-id="26c0e-137">출력</span><span class="sxs-lookup"><span data-stu-id="26c0e-137">OUTPUTS</span></span>

### <span data-ttu-id="26c0e-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="26c0e-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="26c0e-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="26c0e-139">NOTES</span></span>
* <span data-ttu-id="26c0e-140">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 데이터, 팩터리</span><span class="sxs-lookup"><span data-stu-id="26c0e-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="26c0e-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="26c0e-141">RELATED LINKS</span></span>

<span data-ttu-id="26c0e-142">[New-AzDataFactoryGateway](./New-AzDataFactoryGateway.md) 
 [Get-AzDataFactoryGatewayAuthKey](./Get-AzDataFactoryGatewayAuthKey.md)</span><span class="sxs-lookup"><span data-stu-id="26c0e-142">[New-AzDataFactoryGateway](./New-AzDataFactoryGateway.md)
[Get-AzDataFactoryGatewayAuthKey](./Get-AzDataFactoryGatewayAuthKey.md)</span></span>

