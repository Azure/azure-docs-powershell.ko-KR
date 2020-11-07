---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2B4A3E2A-1868-492F-9F77-932319D2CE6D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvpnclientpackage
schema: 2.0.0
ms.openlocfilehash: 193353a3e578ec0f644be605498214d5bf4944c6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881406"
---
# <span data-ttu-id="866d7-101">Get-AzureRmVpnClientPackage</span><span class="sxs-lookup"><span data-stu-id="866d7-101">Get-AzureRmVpnClientPackage</span></span>

## <span data-ttu-id="866d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="866d7-102">SYNOPSIS</span></span>
<span data-ttu-id="866d7-103">VPN 클라이언트 패키지에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="866d7-103">Gets information about a VPN client package.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="866d7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="866d7-104">SYNTAX</span></span>

```
Get-AzureRmVpnClientPackage -ResourceGroupName <String> -VirtualNetworkGatewayName <String>
 -ProcessorArchitecture <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="866d7-105">설명은</span><span class="sxs-lookup"><span data-stu-id="866d7-105">DESCRIPTION</span></span>
<span data-ttu-id="866d7-106">**AzureRmVpnClientPackage** cmdlet은 가상 네트워크 게이트웨이에서 사용할 수 있는 VPN 클라이언트 패키지에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="866d7-106">The **Get-AzureRmVpnClientPackage** cmdlet gets information about the VPN client packages available from a virtual network gateway.</span></span>
<span data-ttu-id="866d7-107">클라이언트 패키지에는 클라이언트 컴퓨터에서 Azure 가상 네트워크에 대 한 VPN 연결을 설정할 수 있는 구성 데이터가 포함 되어 있습니다. VPN 연결을 만들기 위해서는 클라이언트 컴퓨터에 올바른 구성 패키지가 설치 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="866d7-107">Client packages contain configuration data that enable a client computer to make a VPN connection to an Azure virtual network; client computers must have the correct configuration package installed in order to make a VPN connection.</span></span>
<span data-ttu-id="866d7-108">클라이언트 컴퓨터의 Windows 버전 (예: Windows 7 또는 Windows 10)과 클라이언트 컴퓨터의 프로세서 아키텍처 (AMD64 또는 x86)에 따라 다른 구성 패키지를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="866d7-108">Different configuration packages are available based on the client computer's version of Windows (for example, Windows 7 or Windows 10) and on the client computer's processor architecture (AMD64 or x86).</span></span>
<span data-ttu-id="866d7-109">**AzureRmVpnClientPackage** 를 실행할 때 아키텍처 유형을 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="866d7-109">You must specify the architecture type when running **Get-AzureRmVpnClientPackage**.</span></span>

## <span data-ttu-id="866d7-110">예제의</span><span class="sxs-lookup"><span data-stu-id="866d7-110">EXAMPLES</span></span>

### <span data-ttu-id="866d7-111">예제 1: 프로세서 아키텍처 VPN 클라이언트 패키지에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="866d7-111">Example 1: Get information about a processor architecture VPN client package</span></span>
```
PS C:\>Get-AzureRmVpnClientPackage -ProcessorArchitecture -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -ProcessorArchitecture "Amd64"
```

<span data-ttu-id="866d7-112">이 명령은 ContosoVirtualNetworkGateway 이라는 가상 네트워크 게이트웨이에 저장 된 AMD64 VPN 클라이언트 패키지에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="866d7-112">This command gets information about the AMD64 VPN client packages stored on the virtual network gateway named ContosoVirtualNetworkGateway.</span></span>
<span data-ttu-id="866d7-113">X86 클라이언트 패키지에 대 한 정보를 얻으려면 *ProcessorArchitecture* 매개 변수 값을 x86으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="866d7-113">To get information about the x86 client packages, set the value of the *ProcessorArchitecture* parameter to x86.</span></span>

## <span data-ttu-id="866d7-114">변수</span><span class="sxs-lookup"><span data-stu-id="866d7-114">PARAMETERS</span></span>

### <span data-ttu-id="866d7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="866d7-115">-DefaultProfile</span></span>
<span data-ttu-id="866d7-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="866d7-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="866d7-117">-ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="866d7-117">-ProcessorArchitecture</span></span>
<span data-ttu-id="866d7-118">클라이언트 패키지가 디자인 되는 CPU 아키텍처 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="866d7-118">Specifies the type of CPU architecture that the client package is designed for.</span></span>
<span data-ttu-id="866d7-119">유효한 값은 Amd64 및 X86입니다.</span><span class="sxs-lookup"><span data-stu-id="866d7-119">Valid values are Amd64 and X86.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Amd64, X86

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="866d7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="866d7-120">-ResourceGroupName</span></span>
<span data-ttu-id="866d7-121">가상 네트워크 게이트웨이가 할당 되는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="866d7-121">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>

<span data-ttu-id="866d7-122">리소스 그룹은 인벤터리 관리 및 일반 Azure 관리를 간소화 하기 위해 항목을 분류 합니다.</span><span class="sxs-lookup"><span data-stu-id="866d7-122">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="866d7-123">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="866d7-123">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="866d7-124">클라이언트 패키지 정보가 저장 되는 가상 네트워크 게이트웨이의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="866d7-124">Specifies the name of the virtual network gateway where the client package information is stored.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="866d7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="866d7-125">CommonParameters</span></span>
<span data-ttu-id="866d7-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="866d7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="866d7-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="866d7-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="866d7-128">입력</span><span class="sxs-lookup"><span data-stu-id="866d7-128">INPUTS</span></span>

### <span data-ttu-id="866d7-129">이름</span><span class="sxs-lookup"><span data-stu-id="866d7-129">String</span></span>
<span data-ttu-id="866d7-130">' ResourceGroupName ' 매개 변수는 파이프라인에서 ' String ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="866d7-130">Parameter 'ResourceGroupName' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="866d7-131">이름</span><span class="sxs-lookup"><span data-stu-id="866d7-131">String</span></span>
<span data-ttu-id="866d7-132">' VirtualNetworkGatewayName ' 매개 변수는 파이프라인에서 ' String ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="866d7-132">Parameter 'VirtualNetworkGatewayName' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="866d7-133">출력</span><span class="sxs-lookup"><span data-stu-id="866d7-133">OUTPUTS</span></span>

###  
<span data-ttu-id="866d7-134">**Get-AzureRmVpnClientPackage** 개체의 인스턴스를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="866d7-134">**Get-AzureRmVpnClientPackage** returns instances of the System.String object.</span></span>

## <span data-ttu-id="866d7-135">상속자</span><span class="sxs-lookup"><span data-stu-id="866d7-135">NOTES</span></span>

## <span data-ttu-id="866d7-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="866d7-136">RELATED LINKS</span></span>

[<span data-ttu-id="866d7-137">크기 조정-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="866d7-137">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="866d7-138">Set-AzureRmVirtualNetworkGatewayVpnClientConfig</span><span class="sxs-lookup"><span data-stu-id="866d7-138">Set-AzureRmVirtualNetworkGatewayVpnClientConfig</span></span>](./Set-AzureRmVirtualNetworkGatewayVpnClientConfig.md)


