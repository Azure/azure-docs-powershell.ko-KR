---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C83A0465-45EF-4FCC-B706-D5DF819664F0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkInterface.md
ms.openlocfilehash: 3250aa7f9108436cadbf0f46ab0e36d3a9c094d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525488"
---
# <span data-ttu-id="44a12-101">Remove-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="44a12-101">Remove-AzureRmNetworkInterface</span></span>

## <span data-ttu-id="44a12-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44a12-102">SYNOPSIS</span></span>
<span data-ttu-id="44a12-103">네트워크 인터페이스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="44a12-103">Removes a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="44a12-104">구문과</span><span class="sxs-lookup"><span data-stu-id="44a12-104">SYNTAX</span></span>

```
Remove-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44a12-105">설명은</span><span class="sxs-lookup"><span data-stu-id="44a12-105">DESCRIPTION</span></span>
<span data-ttu-id="44a12-106">**AzureRmNetworkInterface** Cmdlet은 Azure 네트워크 인터페이스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="44a12-106">The **Remove-AzureRmNetworkInterface** cmdlet removes an Azure network interface.</span></span>

## <span data-ttu-id="44a12-107">예제의</span><span class="sxs-lookup"><span data-stu-id="44a12-107">EXAMPLES</span></span>

### <span data-ttu-id="44a12-108">예제 1: 네트워크 인터페이스 제거</span><span class="sxs-lookup"><span data-stu-id="44a12-108">Example 1: Remove a network interface</span></span>
```
PS C:\>Remove-AzureRmNetworkInterface -Name "NetworkInterface1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="44a12-109">이 명령은 리소스 그룹 ResourceGroup1에서 네트워크 인터페이스 NetworkInterface1를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="44a12-109">This command removes the network interface NetworkInterface1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="44a12-110">*Force* 매개 변수는 사용 되지 않으므로 사용자에 게이 작업을 확인 하 라는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="44a12-110">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

### <span data-ttu-id="44a12-111">예제 2: 네트워크 인터페이스 제거</span><span class="sxs-lookup"><span data-stu-id="44a12-111">Example 2: Remove a network interface</span></span>
```
PS C:\>Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" | Remove-AzureRmNetworkInterface -Force
```

<span data-ttu-id="44a12-112">이 명령은 리소스 그룹 ResourceGroup1의 모든 네트워크 인터페이스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="44a12-112">This command removes all network interfaces in resource group ResourceGroup1.</span></span>
<span data-ttu-id="44a12-113">*Force* 매개 변수를 사용 하기 때문에 사용자에 게 확인 메시지가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="44a12-113">Because the *Force* parameter is used, the user is not prompted for confirmation.</span></span>

## <span data-ttu-id="44a12-114">변수</span><span class="sxs-lookup"><span data-stu-id="44a12-114">PARAMETERS</span></span>

### <span data-ttu-id="44a12-115">-Force</span><span class="sxs-lookup"><span data-stu-id="44a12-115">-Force</span></span>
<span data-ttu-id="44a12-116">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="44a12-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="44a12-117">-이름</span><span class="sxs-lookup"><span data-stu-id="44a12-117">-Name</span></span>
<span data-ttu-id="44a12-118">이 cmdlet이 제거 하는 네트워크 인터페이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="44a12-118">Specifies the name of the network interface that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44a12-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="44a12-119">-PassThru</span></span>
<span data-ttu-id="44a12-120">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="44a12-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="44a12-121">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="44a12-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="44a12-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44a12-122">-ResourceGroupName</span></span>
<span data-ttu-id="44a12-123">이 cmdlet이 제거 하는 네트워크 인터페이스를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="44a12-123">Specifies the name of a resource group that contains the network interface that this cmdlet removes.</span></span>

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

### <span data-ttu-id="44a12-124">-확인</span><span class="sxs-lookup"><span data-stu-id="44a12-124">-Confirm</span></span>
<span data-ttu-id="44a12-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="44a12-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44a12-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44a12-126">-WhatIf</span></span>
<span data-ttu-id="44a12-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="44a12-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44a12-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="44a12-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44a12-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44a12-129">-DefaultProfile</span></span>
<span data-ttu-id="44a12-130">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="44a12-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44a12-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44a12-131">CommonParameters</span></span>
<span data-ttu-id="44a12-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="44a12-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44a12-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44a12-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44a12-134">입력</span><span class="sxs-lookup"><span data-stu-id="44a12-134">INPUTS</span></span>

## <span data-ttu-id="44a12-135">출력</span><span class="sxs-lookup"><span data-stu-id="44a12-135">OUTPUTS</span></span>

## <span data-ttu-id="44a12-136">상속자</span><span class="sxs-lookup"><span data-stu-id="44a12-136">NOTES</span></span>

## <span data-ttu-id="44a12-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="44a12-137">RELATED LINKS</span></span>

[<span data-ttu-id="44a12-138">Get-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="44a12-138">Get-AzureRmNetworkInterface</span></span>](./Get-AzureRmNetworkInterface.md)

[<span data-ttu-id="44a12-139">새로운 AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="44a12-139">New-AzureRmNetworkInterface</span></span>](./New-AzureRmNetworkInterface.md)

[<span data-ttu-id="44a12-140">Set-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="44a12-140">Set-AzureRmNetworkInterface</span></span>](./Set-AzureRmNetworkInterface.md)


